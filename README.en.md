# OpenControl Client

[Русский](README.md) | **English**

An independent Android VPN client compatible with Kerio Control. Connect to your network, save separate server and account profiles, and switch between them.

**This project is not a Kerio or GFI product, is not affiliated with either company, and is not supported by them.** Kerio Control, Kerio and GFI are mentioned only to describe compatibility.

This repository contains APK releases and instructions. Application sources are maintained separately.

## Download and install

[Latest release and APK](https://github.com/nr084/opencontrol-client-android-releases/releases/latest)

Android 8.0 or later is required. The APK supports arm64-v8a and x86_64. Version 1.5.1 uses the OpenControl library 0.2.0.

1. Download `OpenControl-client-1.5.1-release.apk` from **Assets**. The **Source code** archives are not needed for installation.
2. Open the APK on Android and allow installation from your browser or file manager if prompted.
3. Install and open OpenControl Client.

## Connect

1. Tap **Add** and enter a profile name.
2. Enter the server IP address or DNS name, port, username and password supplied by your network administrator.
3. Optionally enable **Remember password**. Each profile stores its own credentials.
4. For a server using its own certificate, use the certificate check, verify its SHA-256 fingerprint with your administrator, and confirm trust. Trust is stored separately for each profile.
5. Tap **Connect** and approve the Android VPN permission dialog.
6. The main screen shows the profile name, server address and **IP (VPN)**. Tap **Disconnect** to stop.

On the first connection without a saved fingerprint, verify the certificate and choose **Save and connect**. Credentials are not sent before certificate trust is established.

## Client settings

App selection and excluded networks are global settings that apply to every profile. Save your changes and reconnect to apply them.

### Split tunneling by app

In **Settings**, open the VPN apps selector and enable split tunneling. Choose **Only selected** or **All except selected**, search by app name or package name, select apps and save.

The list contains apps with launcher icons. With split tunneling disabled, all apps can use the VPN. **Only selected** requires at least one installed app. When upgrading from 1.1.0, the active profile's app selection is migrated once to global settings.

### Networks outside the VPN

Enter numeric IPv4 networks in CIDR notation, one per line, for example:

```text
192.168.1.0/24
10.0.0.0/8
```

These networks bypass the VPN for all profiles. Up to 128 networks are supported; IPv6 exclusions are not supported. App selection and network exclusions can be combined.

## Android Quick Settings

Choose and save the default profile for the tile in **Settings**. It is independent of the profile selected on the main screen.

Add the **OpenControl Client** tile using the Android Quick Settings editor. It shows the active connection name and status. Tap to disconnect, or to connect the default profile with one tap without opening the app when the password and certificate trust are saved, Android permissions are granted, and the device is unlocked.

If a password, certificate confirmation or VPN permission is needed, the app opens the relevant dialog. If the default profile is missing or deleted, select it again in settings; another profile is not substituted automatically.

The notification shows the connection name and current **UL** (upload) and **DL** (download) speeds in **Mbps**. The server address and **IP (VPN)** remain on the main screen.

## QR import and export

Tap **Import QR**, grant camera permission and scan the code. You are then asked only for a profile name. The profile QR button exports the saved password or the password entered in the connection field. The QR contains a plaintext password: share it only with trusted recipients.

[QR format and integration prompt for other projects](QR_PROFILE_FORMAT.en.md).

## Background operation and reconnection

In **Settings**, request permission for background operation and approve the Android prompt. Some manufacturers also require unrestricted battery use or autostart permission in system settings.

The VPN runs in a foreground service. Reconnection responds to network availability and waking the device. Retry delays are capped at five seconds and reset after a successful connection. With a saved password, trusted certificate and automatic reconnection enabled, the service can restore the session after Android terminates the process. A user force-stop prevents restoration.

With automatic reconnection enabled, unexpected disconnections and temporary errors retain the intent to stay connected and trigger background recovery until you explicitly disconnect. Credential, certificate, permission and configuration errors require user correction; security checks are not bypassed. Restoring a terminated process requires a saved password.

## Features and statistics

- Multiple server and account profiles.
- Global split tunneling and network exclusions.
- Password encryption using Android Keystore.
- Saved certificate fingerprints for each profile.
- 69 interface languages following Android language settings. New translations are automatic; Romansh is excluded.
- Light and dark themes following system settings.
- Connection statistics and a notification with a disconnect action.
- Screenshots are allowed. **About** shows the application and OpenControl library versions.

Data amounts use **KB/MB**, with 1 KB = 1000 bytes. Upload and download speeds use **Mbps**.

## Updates and feedback

Install a new APK over the existing app to preserve profiles and settings; uninstalling first is unnecessary.

[Report an issue or suggest an improvement](https://github.com/nr084/opencontrol-client-android-releases/issues). Do not post passwords or other confidential information.

[Changelog](CHANGELOG.en.md)

© nr084

[Privacy policy](PRIVACY_POLICY.en.md)
