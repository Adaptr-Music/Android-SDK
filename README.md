# Android-SDK
Android SDK releases

Android SDK is now available in JCenter. Add it to your project by adding following line to your project gradle.build file

```implementation 'com.adaptr.android:player-sdk:0.1.3'```

The default variant of Adaptr SDK uses 2.11.8 exoplayer version. If you require another version of exoplayer you can use different versions of the SDK mapped to different exoplayer versions, the currently avaiable versions are. 
```
implementation 'com.adaptr.android:player-sdk-exo2106:0.1.3'
implementation 'com.adaptr.android:player-sdk-exo290:0.1.3'
implementation 'com.adaptr.android:player-sdk-exo281:0.1.3'
```


Alternatively you can also Download one of the .aar files available [here](https://github.com/Adaptr-Music/Android-SDK/releases).

Open Project level build.gradle and add `flatDir{dirs 'libs'}` like below:

```
allprojects {
   repositories {
      jcenter()
      flatDir {
        dirs 'libs'
      }
   }
}
```

Open app level `build.gradle` file and add .aar file:

```
    dependencies {
       implementation(name:'PlayerSdk-exoDefault-release', ext:'aar')
       // Add dependencies as well
       implementation 'com.google.code.gson:gson:2.8.6'
       implementation 'com.squareup.okhttp3:logging-interceptor:4.9.0'
       implementation 'com.squareup.retrofit2:retrofit:2.9.0'
       implementation 'com.squareup.retrofit2:converter-gson:2.9.0'
       implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-core:1.3.7'
       implementation 'org.jetbrains.kotlinx:kotlinx-coroutines-android:1.3.3'
       // Select exoplayer version according to the aar version
       implementation 'com.google.android.exoplayer:exoplayer-core:2.11.8'
       implementation 'androidx.legacy:legacy-support-v4:1.0.0'
    }
```

Full documentation is available at https://docs.adaptr.com/android/latest/index.html
