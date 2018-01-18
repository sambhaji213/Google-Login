# Google-Login
Android Login with Google is a really useful feature for both the app developer and the user
Today Almost all web and mobile apps allow you to login with Google and Facebook Login. 
Android Login with Google is a really useful feature for both the app developer and the user, since almost everybody tend to have a google and facebook account and moreover with android login with google you don’t need to remember your UserId and password. 
We will be creating a sample Google Login app describing how to integrate google login and retrieve user profile. The user can login using her existing google account. 
Integration of Google Login to the App allows the app developers to perform actions on user behalf.

# Pre-requisites of Android Login with Google API
1. Android Studio installed on your PC (Unix or Windows). You can learn how to install it here.
2. A real time android device (Smartphone or Tablet) configured with Android Studio.
3. A compatible Android device that runs Android 2.3 or newer and includes the Google Play Store or an emolator with an AVD that runs the Google APIs platform based on Android 4.2.2 or newer and has Google Play Services version 8.3.0 or newer.
4. The latest version of the Android SDK, including the SDK Tools component.
5. The project must be configured to compile against Android 2.3 (Gingerbread) or newer.

# Installing/Updating Google Play Services
1. To update/Install The Google Play Services SDK:
2. In Android Studio, select Tools > Android > SDK Manager.
3. Scroll to the bottom of the package list and select Extras > Google Play services.
4. The package is downloaded to your computer and installed in your SDK environment at android-sdk-folder/extras/google/google_play_services.

# Get a Configuration File
The configuration file provides service-specific information for your app. Go to Google Developer’s Page 
[Google Developer’s Page](https://developers.google.com/mobile/add?platform=android&cntapi=signin&cntapp=Defaolt%20Demo%20App&cntpkg=com.google.samples.quickstart.signin&cnturl=https:%2F%2Fdevelopers.google.com%2Fidentity%2Fsign-in%2Fandroid%2Fstart%3Fconfigured%3Dtrue&cntlbl=Continue%20with%20Try%20Sign-In). To get it, you must select an existing project for your app or create a new one. You’ll also need to provide a package name for your app.

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin1.png)

1. Create a new project in android studio project, Name the project Google Login and give it a package name. Choose the activity name as LoginActivity.
2. Now add app name and package name on Google Developers page as shown below.

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin2.png)

3. Click on Choose and configure services button
4. Choose Google Sign-In the service page.

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin3.png)

We will continue on this page, but first, we have to generate digitally signed a public certificate which will be.

# Generate SHA-1 fingerprint
In order to consume google plus services, first we need to enable the Google Plus API on google console and we need to register our digitally signed .apk file’s public certificate in the Google APIs Console.
Java key tool an be used to generate the SHA-1 fingerprint.

1. Open your Adroid studio see on right side Gradle option
2. Click on Gradle option then >> Expand project structure >> Select # app then >> Select # Tasks then >> Select # android then >> Select #signingReport and double click on #signingReport and then check your studio Run ternimal 

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin4.png)

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin5.png)

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin6.png)

5. Enter the SHA-1 ID to the Google developer’s page
6. Click on ENABLE SIGN IN button
7. Click on CONTINUE TO GENERATE CONFIGURATION FILE button
8. This will open download and install configuration page, click on Download google-services.json button

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin7.png)

9. Copy the google-services.json file you just downloaded into the app/ or mobile/ directory of your Android Studio project. as shown in the fig

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin8.png)

# Add Login With Google
Add the dependency to your project-level build.gradle:

**build.gradle**

``implementation 'com.google.android.gms:play-services-auth:11.6.0'``

or

``complie 'com.google.android.gms:play-services-auth:11.6.0'``

Add the plugin to your app-level build.gradle:

**build.gradle**

``apply plugin: 'com.google.gms.google-services'``

Do a gradle -sync by clicking on the button as shown in the figure.

![Screenshot](https://github.com/sambhaji213/Google-Login/blob/master/screenshot/glogin9.png)
