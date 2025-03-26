############## Install React-Native ###############

# npx @react-native-community/cli init LEDControlApp

OR

# expo install expo-dev-client
# expo run:android



################# How to Run Your App Now ################
Since you are using Bluetooth, you need to build a development client instead of using Expo Go. Here’s what to do:

1️⃣ Install Expo Dev Client
Run this in your project:

# npm install -g eas-cli

# eas build:configure


2️⃣ Build a Development Client
------------- For Android, run -----------------

# eas build --profile development --platform android



--------------- For iOS (if on macOS)-------------

# eas build --profile development --platform ios

Wait for it to build, then download and install the .apk (Android) or .ipa (iOS) on your device.

3️⃣ Run Your App on a Real Device
Now, use this command to run your app:

------------->  Connect your phone to your PC using a USB cable. <-------------

Open a terminal and run:

# adb devices
# adb pair <DEVICE_IP>:<PAIRING_PORT> <PAIRING_CODE>
# adb connect <DEVICE_IP>:5555


------------------------> All set, then <--------------------------

# npx react-native run-android

# npx expo start --dev-client


############# Alternative: Use an Emulator ############
If you prefer not to build a .apk, you can run the app using Android Studio’s emulator:

# npx expo run:android
Let me know if you need help with this! 🚀
