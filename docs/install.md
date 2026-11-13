# Installing Lazy Tech Runner

You do this once. After that the app updates itself.

## Part 1: the phone

1. On your phone, open the [Releases page](https://github.com/LazyTechGeek/LazyTechRunner/releases/latest).
2. Tap `LazyTechRunner-phone.apk` to download it.
3. Open the downloaded file. Android will ask whether your browser may install apps. Tap **Settings**, switch on **Allow from this source**, then go back.
4. Tap **Install**. If Play Protect asks, choose **Install anyway**. It asks because the app isn't from the Play Store.
5. Open **Lazy Tech Runner** and allow the permissions it asks for: location, physical activity and notifications.

You can stop here and use the phone on its own.

## Part 2: the watch

Wear OS watches can't open a downloaded file themselves, so the first install is sent from a computer.
It looks long, but each step is small.

### Get the watch ready

1. On the watch, open **Settings → About watch → Software information**.
2. Tap **Software version** five times, until it says developer mode is on.
3. Go back to **Settings → Developer options**.
4. Switch on **ADB debugging**, then **Wireless debugging**. The watch must be on the same Wi-Fi as your computer.

### Get the computer ready

1. Download Google's free [platform-tools](https://developer.android.com/tools/releases/platform-tools) and unzip it.
2. Download `LazyTechRunner-watch.apk` from the [Releases page](https://github.com/LazyTechGeek/LazyTechRunner/releases/latest) into that same folder.
3. Open a terminal (Command Prompt on Windows) in that folder.

### Send the app

1. On the watch, in **Wireless debugging**, tap **Pair new device**. It shows an address and a six-digit code.
2. On the computer, type this using the address from the watch, then enter the code when asked:

   ```
   adb pair 192.168.1.50:37123
   ```

3. Go back one screen on the watch. The main Wireless debugging screen shows a second address. Use that one here:

   ```
   adb connect 192.168.1.50:41234
   ```

4. Install the app:

   ```
   adb install -r LazyTechRunner-watch.apk
   ```

5. When it says **Success**, switch **Wireless debugging** off again. Leaving it on drains the battery.

Open **Lazy Tech Runner** on the watch and allow the permissions: heart rate, physical activity, location and notifications.

## Updates

- **Phone:** Settings → **App updates**. It tells you when a new version is ready and installs it.
- **Watch:** Settings, scroll to the bottom, **Check for updates**. You can also send the update from the phone's App updates page.

The first time, each device asks you to allow Lazy Tech Runner to install updates. That is a one-off.

## Removing it

Uninstall it like any other app. Your runs and routes are deleted with it.
