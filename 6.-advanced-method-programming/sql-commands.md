# SQL Commands

<figure><img src="https://sp-ao.shortpixel.ai/client/to_auto,q_lossless,ret_img,w_450,h_517/https://raverobot.com/wp-content/uploads/2018/11/SQL.jpg" alt="" height="517" width="450"><figcaption><p>A File Open command reading over a .xls file using a SQL query to filter for a specific subset of barcodes</p></figcaption></figure>

An app specialist writing methods in Venus should strive to be somewhat familiar with SQL. Of course you can connect a method to a SQL database through the File commands but that isn’t the end of their usefulness.

When using File commands there is an option for a command string. This string is a SQL query which can be used to filter the input files for just the pieces of data you care about.

For example running a File: Open command to read in a .csv which contains data on four different barcoded plates. You could write a SQL query for just the barcode you are currently interested in and then only read in the results of interest.
