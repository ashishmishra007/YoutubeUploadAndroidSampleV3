YoutubeUploadAndroidSampleV3
============================

Youtube Upload Android Sample using Youtube Data API V3

If you want to upload videos using your apps, you can use Youtube Upload API. 
I searched sample using api v3. but I can't find any sample. 

So I made that. if you have any question, feel free to ask. 

It based on task-android-sample and calendar-android-sample.

reference link 

task-android-sample: 
http://samples.google-api-java-client.googlecode.com/hg/tasks-android-sample/instructions.html

calendar-android-sample : 
http://samples.google-api-java-client.googlecode.com/hg/calendar-android-sample/instructions.html?r=default

google-api-java-client : 
https://code.google.com/p/google-api-java-client/

Getting Started with the YouTube Data API :
https://developers.google.com/youtube/v3/getting-started

YouTube Data API Documentation / Version 3.0 / Videos: insert
https://developers.google.com/youtube/v3/docs/videos/insert?hl=ko


##Register Your Application

You first need to register your Android application and sign up for access to the Google YouTube Data API V3 in the Google APIs Console. First, you need the "Signing certificate fingerprint (SHA1)" for the debug build:

keytool -exportcert -alias androiddebugkey -keystore ~/.android/debug.keystore | openssl sha1

Enter keystore password: android

And for the release build:


keytool -exportcert -alias androiddebugkey -keystore my-release-key.keystore | openssl sha1

Next, register in the Google APIs Console:


Visit the Google apis console

1. If this is your first time, click "Create project..." Otherwise, click on the drop down under the "Google apis" logo at the top left, and click "Create..." under "Other projects"
2. Click on "Services", and change the YouTube Data API V3 status to "ON".
3. Click on "API Access", and then on "Create an OAuth 2.0 Client ID...".
4. Enter a product name and click "Next".
5. Select "Installed application", select "Android", enter com.example.youtubeuploadv3 for "Package name".

Note: The package name must be universally unique to actually register an application. If you try to register a package name in use, you may get an error reading "An unexpected error has occurred." This sample has already been registered, so you will need to change the package name.
Paste the SHA1 fingerprint for the debug certificate above into "Signing certificate fingerprint (SHA1)", and click "Create client ID".
Click "Create another client ID..." and follow the directions from the previous steps, but use the release certificate instead of the debug certificate.


##Setup Project in Eclipse

Prerequisites: install Eclipse, the Mercurial plugin (optional), and the Android plugin.

Preferences:

+ Android: setup SDK location
Window > Android SDK Manager
Check on "Google APIs" under "Android 4.1.6 (API Level 16)"
Check on "Google Play services" under "Extras".
Click on "Install X packages..."

+ Import YoutubeUploadV3 project

File > Import...
Select "General > Existing Project into Workspace" and click "Next"
Click "Browse" next to "Select root directory", find [someDirectory]/YoutubeUploadAndroidSampleV3/YoutubeUploadV3 and click "Next"
Click "Finish"

+ Clean Project (if compile error about missing gen directory)

Select YoutubeUploadV3 project
Project > Clean...
Select "Clean projects selected below"

Click on "OK"

NOTE: you must use a physical device for developing and testing because Google Play services cannot be installed on an emulator.

Run
Right-click on project YoutubeUploadV3
Run As > Android Application
Select the physical device and click OK.
