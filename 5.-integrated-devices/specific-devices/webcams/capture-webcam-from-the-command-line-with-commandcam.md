# Capture webcam from the command line with CommandCam

* Home
* Computing

***

📅 Fri, Oct 6, 2023 ⏲️ \~ 2 minutes



CommandCam is an open-source tool for Windows that allows you to **easily capture still images from a webcam from the terminal**, developed by Ted Burke.

**CommandCam is a very simple tool** but that can sometimes be very useful in a project. We just have to launch a command, and we have our Webcam capture.

For example, imagine that you connect to a computer remotely via SSH, or you want to time the capture of an image, or even react to a motion sensor to take a photo, as if it were an “alarm”.

In these and many other cases, **it is very easy to integrate CommandCam**. We just have to launch a command prompt. And there are a thousand ways and options to launch a command.

CommandCam uses the Microsoft DirectShow API to access the images. So it should be **compatible with most USB cameras**.

### How to use CommandCam? <a href="#how-to-use-commandcam" id="how-to-use-commandcam"></a>

As I said, one of the main features of CommandCam is its simplicity. We just have to run this command,

```
CommandCam /filename output.bmp
```

Where `output.bmp` is the name of the file with which we want to save the capture.

It is also possible to specify a wait time between receiving the command and taking the capture, with the parameter `/delay [milliseconds]`. For example like this,

```
CommandCam /filename output.bmp /delay 10000
```

On the other hand, in the case of having several connected devices, it is possible to choose which one we want to use using the parameter `/devnum [device_number]` like this

```
CommandCam /filename output.bmp /devnum 2
```

Or with the device name using `/devname [device_name]`

```
CommandCam /devname "USB Video Device"
```

We can also get a list of devices compatible with `/devlist`

```
CommandCam /devlist
```

Or the list with more details with the parameter `/devlistdetail`

```
CommandCam /devlist
```

Finally, we can make CommandCam not display any text in the console with the parameter `/quiet`

```
CommandCam /filename output.bmp /quiet
```

CommandCam is written in C++, and the whole application takes up just 550 lines. It is Open Source and all the code and information are available on [GitHub - tedburke/CommandCam](https://github.com/tedburke/CommandCam) and on the [author’s blog](https://batchloaf.wordpress.com/commandcam/).

Topics:

* Software
