# SMS She'rlar

A Kotlin Android app for browsing Uzbek poems by topic and keeping a local collection. The project uses Android Views, fragments, RecyclerViews, and SharedPreferences.

## Features represented in the source

- Categories for love, longing, congratulations, parents, friendship, and humor.
- Lists and detail/navigation behavior for poem content.
- Locally saved poems and favorites serialized through Gson and SharedPreferences.
- An SMS permission/request helper.

The actual `SmsManager` send call in `SendSMSdata.kt` is commented out. SMS sending is not a completed feature in the current helper.

## Source map

- [HomeFragment.kt](app/src/main/java/com/chsd/smssherlar/HomeFragment.kt): category navigation and local counts.
- [adapters/](app/src/main/java/com/chsd/smssherlar/adapters/): category and poem lists.
- [models/SharedPref.kt](app/src/main/java/com/chsd/smssherlar/models/SharedPref.kt): local serialized collections.
- [models/SendSMSdata.kt](app/src/main/java/com/chsd/smssherlar/models/SendSMSdata.kt): SMS-related placeholder behavior.

## Build

Open the repository in Android Studio and use the checked-in Gradle wrapper. The app currently declares compile SDK 31 and minimum Android API 23; install the matching Android SDK and use a JDK compatible with the project's Android Gradle Plugin.

```sh
./gradlew :app:assembleDebug
```

This command is a build entry point, not a recorded passing build. The project retains its original dependency versions, so Gradle sync or dependency updates may be needed with a current Android Studio installation.

The project retains Kotlin Android Extensions and older Android libraries. Current device behavior and local-data restoration have not been verified.
