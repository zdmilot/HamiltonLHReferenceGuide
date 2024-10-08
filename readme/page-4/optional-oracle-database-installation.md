# Optional Oracle Database Installation

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE</p><p>The Installation of an Oracle Database requires the installation of the VENUS Database Plus 1.1 package. VENUS Database Plus 1.1 is a tool to track samples over multiple runs or multiple instruments throughout the lab. Database plus can be used on both local and remote servers. It allows easy access to run data, reliable sample tracking and customized reporting.</p></td></tr></tbody></table>

To set up a database connection with an Oracle server, the Oracle server has to be installed and connected first. Also, a local client has to be installed (up to version 11g).

<table data-header-hidden><thead><tr><th width="145"></th><th></th></tr></thead><tbody><tr><td><img src="../../.gitbook/assets/image (10) (1) (1) (1) (1).png" alt="" data-size="original"></td><td><p>NOTE </p><p>For Oracle installation and server set-up, please refer to the appropriate Oracle information: www.oracle.com</p></td></tr></tbody></table>

\


## Example for Oracle Services (TNS name orcl)

1.  Open the Vector Database Connection Settings found in the System Settings of the Hamilton System Configuration Editor and switch the database server type to Oracle.

    <figure><img src="../../.gitbook/assets/image (38) (1).png" alt="" width="563"><figcaption></figcaption></figure>
2.  Enter the TNS name of the server into the Host String text field and specify a username and password.

    <figure><img src="../../.gitbook/assets/image (39) (1).png" alt="" width="428"><figcaption></figcaption></figure>
3.  Type in the settings specified in the image below.

    <figure><img src="../../.gitbook/assets/image (40) (1).png" alt="" width="428"><figcaption></figcaption></figure>

    Values taken out from the example screen above:

    TNS Name:  orcl \
    Username:  Hamilton \
    Password:  mkdpw:V43

    \
    Alternatively, a host string can be used if there is no TNS name matching to the host string, for example: (DESCRIPTION=(ADDRESS\_LIST=(ADDRESS=(PROTOCOL=TCP)(HOST=172.16.110.200)(PO RT=1521)))(CONNECT\_DATA=(SIC=orcl)))
4.  Prepare the server for the connection. Enter the username and password of the server administrator.\


    <figure><img src="../../.gitbook/assets/image (41) (1).png" alt="" width="270"><figcaption></figcaption></figure>
5.  Confirm to build up the database server.

    <figure><img src="../../.gitbook/assets/image (42) (1).png" alt="" width="339"><figcaption></figcaption></figure>
6.  The dialog message should be prompted right after.\


    <figure><img src="../../.gitbook/assets/image (43) (1).png" alt="" width="249"><figcaption></figcaption></figure>
7. The database connection can be checked using the \[Test Connection] Button found in the “Vector Database Connection Settings”.
