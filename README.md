# Android-SDK
Android SDK releases

Download one of the .aar files available [here](https://github.com/Adaptr-Music/Android-SDK/releases).

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
    }
```

Full documentation is available at https://docs.adaptr.com/android/latest/index.html
