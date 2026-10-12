# Changelog

[Русский](CHANGELOG.md) | **English**

## 1.5.0 — 2026-10-12

- Interface localization for 69 languages and variants for 85 Google Play locales.
- Existing Russian and English UI retained; new translations are automatic. Romansh is excluded.
- Store icon, feature graphic and real phone, 7-inch and 10-inch tablet screenshots in Russian and English.
- Translated Google Play listings and a signed AAB.

This release does not resolve the reported 600-second disconnection on Kerio Control 9.4.3 build 8353.

## 1.4.1 — 2026-10-11

- Automatic reconnection retains the intent to stay connected after unexpected disconnections, network changes and temporary errors.
- Credential, certificate, permission and configuration errors require user correction without silently disabling automatic connection.
- Explicit disconnection cancels scheduled recovery attempts.
- New release filenames use the `OpenControl-client-` prefix.

## 1.4.0 — 2026-10-11

- Profile QR export and camera import, asking only for the profile name.
- Published QR format v1 and an integration prompt for other projects.
- Faster reconnection: reset delays after success, cap retry delays, and react immediately to network and wake events.
- Losing an unrelated network no longer interrupts a working connection.
- Background operation permission and saved session restoration by the Android service.

## 1.3.0 — 2026-10-10

- Notifications show current UL/DL speeds in Mbps instead of server and VPN IP addresses, while retaining the connection name.
- A default profile setting for Android Quick Settings.
- One-tap connection of a prepared default profile without opening the app, independently of the profile selected on the main screen.

## 1.2.0 — 2026-10-10

- Android Quick Settings tile to toggle the VPN and show the active connection name.
- **Save and connect** on the first connection without a saved certificate fingerprint.
- Split tunneling moved to global client settings, applying to all profiles.
- Global IPv4 network exclusions.
- Data amounts in KB/MB and transfer speeds in Mbps.
- Documentation uses the **OpenControl Client** name.

## 1.1.0 — 2026-10-10

- Native Android split tunneling with **Only selected** and **All except selected** modes.
- VPN app settings, app search and per-profile selection; changes apply on the next connection.
- Notification icon changed to a hollow shield outline without an exclamation mark.

## 1.0.0 — 2026-10-10

- First public release of OpenControl Client, compatible with Kerio Control.
- Separate server and account profiles, saved passwords and certificate fingerprints.
- Russian and English interface with system light and dark themes.
- Tunnel address labeled **IP (VPN)** in the app and notification.
- **About** dialog with a description, application and OpenControl library versions, copyright and the Kerio/GFI independence disclaimer.

This project is not a Kerio or GFI product and is not affiliated with either company.
