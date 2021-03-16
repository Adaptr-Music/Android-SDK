# Android-SDK
Android SDK releases

Android SDK is now available through Jitpack. [![](https://jitpack.io/v/adaptr-music/AndroidSDK.svg)](https://jitpack.io/#adaptr-music/AndroidSDK)

Add it in your root build.gradle at the end of repositories:

	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}

Add it to your project by adding following line to your project gradle.build file

```implementation 'com.github.Adaptr-Music.Adaptr-AndroidSDK:player-sdk:version'``` [![](https://jitpack.io/v/adaptr-music/AndroidSDK.svg)](https://jitpack.io/#adaptr-music/AndroidSDK)

The default variant of Adaptr SDK uses 2.13.1 exoplayer version. If you require another version of exoplayer you can use different versions of the SDK mapped to different exoplayer versions, the currently avaiable versions are. 
```
implementation 'com.github.Adaptr-Music.AndroidSDK:player-sdk-exo2118:0.1.6'' // Exoplayer version 2.11.8
implementation 'com.github.Adaptr-Music.AndroidSDK:player-sdk-exo2106:0.1.6'' //  Exoplayer version 2.10.6 
implementation 'com.github.Adaptr-Music.AndroidSDK:player-sdk-exo290:0.1.6'' // Exoplayer version 2.9.0
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
