# Smartable Wallet for Android

Official Android builds of [Smartable Wallet](https://getsmartable.app), a
non-custodial wallet: no company holds your keys — not even us.

This project holds releases only: the APK and how to check it. It has no source
code, because the application is not open source. Its open-source core — the
key core that holds the keys and signs, encrypted storage, the app PIN and
lockout, biometric unlock and split backup — is published separately as
[Smartable Wallet Core](https://github.com/getsmartableapp/core) (also on
[GitLab](https://gitlab.com/getsmartable-app/core)), under the Apache License
2.0, and every release names the core version it carries.

## Download

From [getsmartable.app/get](https://getsmartable.app/get), from
[Releases](https://github.com/getsmartableapp/android/releases) here, or from
the same project's [releases on GitLab](https://gitlab.com/getsmartable-app/android/-/releases),
where the website's download button leads. Each release carries the same file,
with the same checksum.

Requires Android 11 or later on a 64-bit ARM phone (arm64-v8a).

## Check the file before installing

Each release lists the APK's SHA-256 checksum and the SHA-256 fingerprint of
its signing certificate. The current release, 3.0.1 (build 24), is signed with
this certificate:

```text
a620bbde76e011db72c5ded72c4c4dc37ab57fb02f91ac840286bd628568e335
```

It is also published on [getsmartable.app](https://getsmartable.app/get).

1. The file is the one the release lists — download the APK and `SHA256SUMS`
   from the release into one folder:

   ```bash
   sha256sum -c SHA256SUMS          # macOS: shasum -a 256 -c SHA256SUMS
   ```

2. The file is signed with the certificate its release lists — `apksigner`
   comes with the Android SDK build tools:

   ```bash
   apksigner verify --print-certs smartable-X.Y.Z-N.apk
   ```

   "Signer #1 certificate SHA-256 digest" must read the certificate SHA-256
   the release lists — for 3.0.1 (build 24), the value above.

Android installs an update over an existing copy only when it is signed with
the same key, so a file signed by anyone else cannot replace the app you have.

## Updates

The app does not update itself. New versions are published here and on
getsmartable.app, each with its checksum and signing certificate fingerprint.

## Security

Report a vulnerability privately, by email to
[hello@getsmartable.app](mailto:hello@getsmartable.app) — never in public.
Help with the app: [getsmartable.app/help](https://getsmartable.app/help).

## Terms

Use of the application is governed by the
[Terms of Use](https://getsmartable.app/terms) and the
[Privacy Policy](https://getsmartable.app/privacy). The names "Smartable" and
"Smartable Wallet", the logo and the app icon are not licensed.
