# VENUS Video Recorder Library

‌Overview

The VENUS Video Recorder library is a custom library that allows video recording/capture from an attached camera device (e.g., Webcam) or desktop recording.

\


‌Download Materials

[VENUS Video Recorder Library](https://download.hamiltonsupport.com/wl/?id=NoIXHT3S8aPLjhvyG20rW3P0y3ONc6Wp)

\


‌Installation

The installer will add the library and associated files to the HAMILTON\Library\VideoRecorder folder. An XVid video codec will also be installed, this is to reduce the overall file size of the captured videos.

Virtual Dub will automatically be included in the HAMILTON\Library|VideoRecorder\VDub folder and needs to be configured to desired settings

\


1. ## Open Veedub64.exe from the above folder
2.  ## Click File --> Capture Avi to go to capture settings

    \


    ![Graphical user interface, application, Word  Description automatically generated](blob:https://app.gitbook.com/95d00aed-f9cf-4811-b3d1-48f225e9db54)
3.  Click Device and make a note of the desired video input name e.g., "USB Video Device" (this will be needed in the initialization step of the library later). If you select a device it will display in the window, so this can be used to check the desired device name.

    \


    ![Graphical user interface, website  Description automatically generated](blob:https://app.gitbook.com/0c7e7e0d-8331-4962-bd19-88649a26d56b)
4.  Click Video --> Compression, select XVid MPEG-4 Codec (this will create compressed video files that take less disk space). Click Configure --> Other Options... and uncheck "Display encoding status" this will remove an annoying pop up that would otherwise run each time the library is used. Click OK on all open windows to save.

    \


    ![Graphical user interface, application  Description automatically generated](blob:https://app.gitbook.com/cbe0fdae-fa6f-4652-8812-633f48f0de86)

    \


    ![A screenshot of a computer  Description automatically generated with medium confidence](blob:https://app.gitbook.com/0f4b5bec-0d35-4e2e-9657-d94edc045b30)
5.  Click Video --> Set custom format, then you can select your desired resolution etc., the video output will be visible in the main window, giving an indication of what will be recorded. Click OK on open windows to save.

    ![Graphical user interface, application  Description automatically generated](blob:https://app.gitbook.com/0dce4f17-f394-4384-be19-9f7acac9670d)

    \


    ![Graphical user interface  Description automatically generated](blob:https://app.gitbook.com/e9a4a5e0-4c26-4276-bb60-dfede00c8402)
6. You can now close VirtualDub and the capture settings will be saved.

You will find a test method in the HAMILTON\Methods\VideoRecorder folder

‌Dependencies

Hamilton VENUS Software Virtual Dub

XVid Codec

\


‌Library Functions

The VENUS Video Recorder library is a submethod library that contains Initialize, Start and Stop record steps.

\


![Graphical user interface, text  Description automatically generated](blob:https://app.gitbook.com/8da550e2-b529-4966-990e-38d817976034)

The initialize requires the name (as a string) of the desired capture device (see above) and a location folder to store the output videos.

\


![Graphical user interface, text, application, email  Description automatically generated](blob:https://app.gitbook.com/75ac6a69-f081-4cac-afa2-1e8a7923c0c1)

The start step will record using the capture device until told to stop. It's recommended to put a StopRecord step in the On Abort tab for this reason.

‌Additional Information

[Virtual dub and supporting help can be found here ](https://www.virtualdub.org/)[Virtual Dub](https://www.virtualdub.org/)

[XVid codec can be found here ](https://xvid-codec.en.softonic.com/)XVid Codec (other codecs can be used if there is a preferred one, settings just need to be changed in the VDub software)

[VLC Media Player may be necessary to view created videos ](https://www.videolan.org/)[VLC Media Player](https://www.videolan.org/)
