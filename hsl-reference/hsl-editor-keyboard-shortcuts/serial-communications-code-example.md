# Serial Communications Code Example

```clike
/*

This program demonstrates the serial communication with a RS-232 scanner.

The program is for demonstration purposes only. It is only intended to 

prove that cabling is correct, the COM port and the scanner are working. 

If the bar code data is displayed on the screen while using this 

program, it only demonstrates that the hardware interface and scanner are 

working.

The program negotiates with the scanner to use ACK/NAK flow control and 

STX/ETX data formating. When the ACK/NAK option is enabled, the executor will not transmit again unless an ACK (ASCII 006) is received after data transmission. If a NAK (ASCII 021) is received, the executor will retransmit the data.

When STX/ETX option is enabled, the executor will transmit a STX (ASCII 002) 

character before transmitting the data and an ETX (ASCII 003) character 

immediately following a data transmission, and remove a STX immediately preceding data reception and remove an ETX immediately following a data reception.

*/

 

method Main()

{

file port;               /* communications port */

variable barcode("");    /* place to read barcodes from the scanner */

 

/* Specify the timeout values */

 

/*

Remarks:

A value of hslInfinite, combined with zero values for both the

ReadTotalTimeoutConstant and ReadTotalTimeoutMultiplier members, 

specifies that the read operation is to return immediately 

with the characters that have already been received, even if no 

characters have been received. 

 

If an application sets ReadIntervalTimeout and ReadTotalTimeoutMultiplier 

to hslInfinite and  sets ReadTotalTimeoutConstant to a value greater 

than zero and less than hslInfinite, one of 

the following occurs when the ReadRecord function is called: 

If there are any characters in the input buffer, ReadRecord returns immediately with the characters in the buffer. 

If there are no characters in the input buffer, ReadRecord waits until a character arrives and then returns immediately. 

If no character arrives within the time specified by ReadTotalTimeoutConstant, ReadRecord times out. 

*/

 

variable ReadIntervalTimeout(hslInfinite);        /* maximum time between read chars */

variable ReadTotalTimeoutMultiplier(hslInfinite); /* multiplier of characters */

variable ReadTotalTimeoutConstant(10.000);        /* constant in seconds */

variable WriteTotalTimeoutMultiplier(0.000);      /* multiplier of characters */

variable WriteTotalTimeoutConstant(10.000);       /* constant in seconds */

 

/* Open the port */

 

port.SetDelimiter(hslAsciiText);

port.AddField(1, barcode, hslString);

port.Open("COM2 9600,S,7,2,ACK/NAK,STX/ETX", hslWrite);

 

/* Set the timeouts */

 

SetCommTimeouts(port);

 

/* Configurate the scanner */

 

if (!port.WriteString("999999"))   /* enter configuration mode */

{

MessageBox("WriteString failed", "ERROR", hslError);

abort;

}

if (!port.WriteString("118414"))   /* enable fast beep */

{

MessageBox("WriteString failed", "ERROR", hslError);

abort;

}

if (!port.WriteString("318515"))   /* optional tone 6 */

{

MessageBox("WriteString failed", "ERROR", hslError);

abort;

}

if (!port.WriteString("999999"))   /* exit configuration mode */

{

MessageBox("WriteString failed", "ERROR", hslError);

abort;

}

 

/* Read barcodes */

 

while (1)

{

barcode = "";

if (!port.ReadRecord())

{

MessageBox("ReadRecord failed", "ERROR", hslError);

abort;

}

Trace("barcode = ", barcode);

}

 

return;

}

```

