# How to Pass In Data to a Shell Command

It looks like you're using a shell in an interface to execute a `.bat` script (like `notify.bat`). If you want to pass variables or parameters to the `curl` command inside the `.bat` file, you can modify the batch script to accept command-line arguments.

Here’s how to pass variables to a `.bat` file and use them in your `curl` command:

#### Modify the Batch Script (`notify.bat`)

Assume you want to pass two arguments to the batch script (for example, a message and a URL). You can modify your `notify.bat` script like this:

```bat
@echo off
set message=%1
set url=%2

curl -X POST -d "message=%message%" %url%
```

#### Explanation:

* `%1` refers to the first argument passed to the batch script (for example, the message).
* `%2` refers to the second argument passed to the batch script (for example, the URL).
* The `curl` command posts the message to the provided URL using the `-d` flag for sending data.

#### Example of How to Pass Variables

In the shell command where you reference the `.bat` file, you would provide arguments after the `.bat` path. For example:

```
Files (x86)\HAMILTON\Methods\AccQ\notify.bat "Hello World" "http://example.com/endpoint"
```

In this example:

* `"Hello World"` is the message.
* `"http://example.com/endpoint"` is the URL to which the `curl` command sends the data.

#### Adjusting in Your Shell Editor:

In the interface you provided, you can include the variables you want to pass to the batch file as part of the "Program" field where you specify the script. For example, modify the command like this:

```
Files (x86)\HAMILTON\Methods\AccQ\notify.bat "YourMessage" "https://your-api-url.com"
```

Make sure the `.bat` file is set up to handle those parameters as shown above. This way, you can dynamically change what message or URL is passed into the `curl` command.

