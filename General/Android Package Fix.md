# Fix "App Not Installed – Package Conflicts" on Android (No PC)

1. **Enable Developer Mode**

   * Settings → About Phone → tap **Build Number** 7 times

2. **Enable USB Debugging**

   * Developer Options → **USB Debugging → ON**

3. **Install Termux**

   * Go to [F-Droid](https://f-droid.org) and click Download F-Droid. Install the APK.
   * Go back to F-Droid and scroll down to Find Apps.
   * Search for **Termux**, scroll down until you see that exact result, and install it.

4. **Prepare Termux**

   * Open Termux
   * Update packages:

     ```
     pkg upgrade
     ```
   * Install ADB tools:

     ```
     pkg install android-tools
     ```

5. **Enable Wireless Debugging**

   * Developer Options → **Wireless Debugging → ON + Allow the connection**
   * Tap **Pair device with pairing code**

6. **Pair Termux/ADB with Your Device**

   * In Termux, run:

     ```
     adb pair IP:PAIRING_PORT
     ```

     * Enter the pairing code shown on the phone
   * Connect to the main port:

     ```
     adb connect IP:MAIN_PORT
     ```

7. **Uninstall the Conflicting App**
     ```
     adb uninstall com.roblox.client
     ```
