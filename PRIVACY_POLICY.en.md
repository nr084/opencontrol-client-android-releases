# OpenControl Client Privacy Policy

[Русский](PRIVACY_POLICY.md) | **English**

Effective date: **October 13, 2026**. This policy describes OpenControl Client for Android, package `org.opencontrol.android`, version 1.5.2.

Developer: **nr084**. Privacy contact: **[arag0rn.smart@gmail.com](mailto:arag0rn.smart@gmail.com)**.


The server is a private corporate firewall administered by the network owner, not a public VPN service provided by this project. The app asks for separate consent to its VPN data flow before first VPN use. The privacy policy is accessible from About and that disclosure. The consent version is stored locally; clearing app data removes it.

## Purpose

OpenControl Client is an independent VPN client that connects to a server specified by the user. The developer does not provide VPN servers or operate your network's server. The project is compatible with Kerio Control but is not a Kerio or GFI product, is not affiliated with either company and is not supported by them.

## Data processed by the client

On your device, the app processes:

- Profile names, server addresses and ports, usernames and entered passwords.
- CA certificates and approved server certificate fingerprints.
- Split tunneling app selections, excluded networks and the default profile.
- Connection state, assigned VPN address, routes, DNS servers, traffic amounts and speeds, app/library/Android versions and device architecture.
- Network packets from apps permitted to use the VPN, for forwarding through the tunnel.

These data are used for connection, server verification, routing, reconnection and status display. To populate the app selector, the client reads the local list of apps with launcher icons. This list is not sent to the developer or VPN server.

## Data transmission and recipients

To sign in, the client sends your username and password to your chosen VPN server over a protected control connection after server certificate trust has been verified. The server also receives necessary protocol information, including the client and Android versions, and sees the connection's network address.

App traffic is routed through the VPN according to your app and network settings. The tunnel between the client and server is encrypted. Your VPN administrator and the operators of network services you access may process traffic, DNS queries and connection information under their own configurations and policies. A VPN alone does not provide end-to-end encryption from its server to every website; this depends, for example, on HTTPS. The operating system's DNS mechanisms resolve the VPN server's hostname.

The client has no ads, embedded analytics or automatic crash reports to the developer. It does not send passwords, profiles, app lists or browsing history to the developer and does not use traffic for advertising or selling data. The developer does not receive VPN traffic contents unless you independently choose a server operated by the developer.

## Local storage and protection

Profiles and settings are stored in the app's private Android storage. Saved passwords are separately encrypted with AES-GCM using an Android Keystore key. Profile names, addresses, usernames and other settings are not claimed to be separately encrypted.

When password remembering is disabled, the client does not store the password persistently; it is processed in memory for the current session. Restoring a session after process termination requires a saved password. Session restoration stores a profile identifier and any user-intervention state, not a plaintext password.

Automatic app data backup is disabled in the Android configuration. Screenshots are permitted; screenshots taken by users may contain profile information and should be handled appropriately.

## Camera and QR codes

Camera permission is used when opening the profile QR scanner. The app does not save or upload camera images. Decoded data are processed locally and saved as a new profile after you provide a name. Imported passwords are encrypted in the same way as other saved passwords.

An exported QR code contains the server address, username and **plaintext password**. Export is initiated by the user. The image is displayed and is not sent automatically; share it only with trusted recipients. QR images or screenshots saved by the user are not deleted when a profile is deleted.

## Retention and deletion

- Profiles and settings remain until you delete or change them, clear app data or uninstall the app.
- Deleting a profile removes its record and saved password. Turning off password remembering and saving the profile removes that profile's saved password.
- Current traffic statistics are used in memory for status display; the client does not create browsing history.
- To remove all local app data, use Android's Clear storage/Clear data function or uninstall the app.
- The client does not create an account with the developer. Deleting a profile does not delete accounts or logs on the VPN server; contact its administrator for those requests.

## Support and external services

If you independently email the developer, your email address, message and attachments are processed to handle your inquiry and necessary follow-up responses. You may request deletion of correspondence held by the developer using the privacy contact. Records that must be retained under applicable law may be kept for the required period. Do not send passwords or private keys. The developer cannot access or remotely delete your device's local profiles.

Email is handled by Google Gmail. Public project pages and issues are hosted on GitHub. Their own privacy policies apply when you use these services: [Google](https://policies.google.com/privacy) and [GitHub](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement). Public issues are visible to others; do not include confidential information. The client does not automatically send support emails or create issues.

## Policy changes

Changes are published on this page with an updated date. Material changes to data processing must be reflected in this policy and any required in-app notices before that processing begins.

For data processing or deletion inquiries, email **arag0rn.smart@gmail.com**.
