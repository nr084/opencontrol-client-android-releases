# OpenControl Client: profile QR format v1

[Русский](QR_PROFILE_FORMAT.md) | **English**

The QR contains plain UTF-8 JSON, without a URI wrapper or Base64:

```json
{"type":"opencontrol-profile","version":1,"ip":"vpn.example.org","port":4090,"login":"user","password":"example-password"}
```

These are sample values, not real credentials.

| Field | Type | Rule |
|---|---|---|
| `type` | string | Exactly `opencontrol-profile` |
| `version` | integer | Exactly `1` |
| `ip` | string | Server IP or DNS name without a URL scheme, at most 253 characters |
| `port` | integer | Optional; defaults to 4090; range 1–65535 |
| `login` | string | Nonempty, at most 1024 UTF-8 bytes, no NUL |
| `password` | string | Nonempty, at most 1024 UTF-8 bytes, no NUL |

The entire JSON must be at most 2500 UTF-8 bytes. Use standard JSON escaping and QR byte mode with UTF-8 encoding. Do not trim or normalize credentials. Unknown additional fields are ignored. Do not include a profile name: after scanning, the client asks only for a name, creates a new profile, and encrypts the saved password using Android Keystore. Certificate trust is not imported; normal fingerprint confirmation applies on the first connection.

The QR contains a plaintext password. Share it only with trusted recipients. Never put the JSON or QR image in logs, telemetry, public documents or repositories. The client scanner passes only a one-use token between activities; QR contents remain in process memory.

## Ready-to-use prompt for another project

> Add VPN profile export to a QR code compatible with OpenControl Client. The QR must contain plain UTF-8 JSON without a URL wrapper or Base64. Format: `{"type":"opencontrol-profile","version":1,"ip":"vpn.example.org","port":4090,"login":"user","password":"example-password"}`. Use the exact fixed type/version values. ip is the server IP or DNS name without a URL scheme. port is an optional integer from 1 to 65535, defaulting to 4090. login/password are nonempty strings of at most 1024 UTF-8 bytes each, without NUL. Preserve Unicode, whitespace and special characters; use standard JSON escaping. Limit the entire JSON to 2500 UTF-8 bytes. Do not include the profile name: the importing client asks for it separately. Generate UTF-8 QR codes and verify decoding back to the original payload. Do not write credentials or QR images to logs, telemetry or files without explicit user action. When displaying a QR, explain that it contains a password and is intended only for trusted recipients.
