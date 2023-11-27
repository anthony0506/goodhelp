# goodhelp
React Native donation app

This is collaborating with Nathan Chackerian.

Android Google Map key=

------------
emulator -list-avds
emulator -avd <--emulator_name-->

------------
yarn install
yarn start

------------
npm install -g eas-cli      // install eas
npm expo-doctor             // check project
npx expo install --check    // review and upgrade your dependencies

eas login
eas whoami
eas build:configure
eas build --platform android/ios/all
eas submit

------------
Build an apk, not aab file
eas.json
{
  "cli": {
    "version": ">= 5.6.0"
  },
  "build": {
    "preview": {
      "android": {
        "buildType": "apk"
      }
    },
    "preview2": {
      "android": {
        "gradleCommand": ":app:assembleRelease"
      }
    },
    "preview3": {
      "developmentClient": true
    },
    "production": {
      "android": {
         "buildType": "apk"
      }
    }
  },
  "submit": {
    "production": {}
  }
}