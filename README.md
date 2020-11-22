# Android-SDK
Android SDK releases

Download the attached aar file to libs folder.

then in app build.gradle specify following and click sync project with Gradle files. Open Project level build.gradle and add flatDir{dirs 'libs'} like below
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
and now open app level build.grdle file and add .aar file

    dependencies {
       implementation(name:'PlayerSdk-exoDefault-release', ext:'aar')
    }

Full documentation is available at https://docs.adaptr.com/android/latest/index.html
