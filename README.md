sample vue native using native base , camera , maps

Specify your Google Maps API Key:
source : https://github.com/fqborges/react-native-maps/blob/master/docs/installation.md#on-ios
Add your API key to your manifest file (android/app/src/main/AndroidManifest.xml):

<application>
    <!-- You will only need to add this meta-data tag, but make sure it's a child of application -->
    <meta-data
      android:name="com.google.android.geo.API_KEY"
      android:value="Your Google maps API Key Here"/>
</application>

1. clone from git clone links

2. that is my sdk
3. wait after install module using yarn / npm , iam using yarn :)
4. use simulation using geny motion
5. set metwork to bridge and choice your ethernet/wireless card 
6. set virtual box to bridge adaptor and reopen genymotion
7. run on your directory root project react-native run-android
8. make sure your opengapps is enable on genymotion
9. get credential code from google api sdk to enable maps
10. enable camera , i am using dummy

------------------- Firebase Setup --------------------

1. Sign up for firebase console and create a new project using '+' button in firebase console.
2. Enter project name and click on create project button.
3. Allow google analytics if you want.

-------------------- Android ----------------

1. After creating a successful project, open project's dashboard and click on android icon and follow the steps.
2. Add applicationId of your project ( present in build.gradle file of android folder ), add a nickname and SHA - debug key (Optional).
3. Download google-services.json file and place it inside app folder of android.
4. open your vue-native project using terminal and npm install react-native-firebase.
5. Then run command react-native link react-native-firebase.
6. Add the following dependencies to android/app/build.gradle file implementation "com.google.android.gms:play-services-base:16.1.0" implementation "com.google.firebase:firebase-core:16.0.9" implementation "com.google.firebase:firebase-auth:17.0.0" implementation "com.google.firebase:firebase-firestore:19.0.0" Also add, apply plugin: 'com.google.gms.google-services'on the top of this file.
7. Add the following line to android/build.gradle file. classpath 'com.google.gms:google-services:4.2.0'
8. Change classpath 'com.android.tools.build:gradle:3.4.0' to ``classpath 'com.android.tools.build:gradle:3.4.1'` in android/build.gradle file.
9. Add method google() in allprojects/repositories in build.gradle file.
10. Open MainApplication.java file and add lines new RNFirebaseAuthPackage(), new RNFirebaseFirestorePackage() inside getPackages() function.
11. Add subsequent imports to above packages in MainApplication.java file import io.invertase.firebase.auth.RNFirebaseAuthPackage; import io.invertase.firebase.firestore.RNFirebaseFirestorePackage;
12. run command react-native run-android to run the project.



---------------------- IOS -----------------------

1. Open your project in firebase console and click on add app + button. A new screen will open.
2. First add the BundleId (can be found in Xcode>project.xcworkspace>general>bundle identifier) of your project, project nickname and apple id (Optional).
3. Then download Google-Service-Info.plist file in the next step and add it using Xcode. Open Xcode> Click on your project name after opening project.xcworkspace file> click on folder with same name as project and select add files to project_name>Add Google-Service-Info.plist file.
4. Now open terminal > ios folder > podfile. If pod file is not created, create a new one using command pod init.
5. Add pod Firebase/Core and pod Firebase/Analytics to podfile.
6. Add lines @import Firebase and [FIRApp configure] to AppDelegate.m file of your project.(Remove one use_frameworks from pod if found more than one )
7. Run pod install.
8. Open .xcworkspace file of your project and click on play button.