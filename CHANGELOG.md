# Changelog

All notable changes to BISM Wallet release binaries are recorded here.
Versions are the Android `versionName` (`versionCode`); each is published as a
GitHub Release tagged `wallet-vX.Y.Z`.

## [wallet-v1.0.0] — 2026-10-09

First public release of the BISM Wallet Android app (`com.bismify.bism`).

- **Signed** with the BISM release key (application id `com.bismify.bism`,
  label `BISM Wallet`); installs/updates in place under the same certificate.
- **Self-custodial key model:** 24-word BIP39 seed phrase + 6-digit PIN, with a
  device vault key protected by Android Keystore.
- **BISM-only:** the wallet targets the BISM networks (mainnet default, plus
  testnet/devnet/lightnet) from the bundled network registry; legacy Mina/Zeko
  networks were removed.
- **Send / receive / delegate** BISM; in-app browser zkApp interaction via the
  standard `window.mina` provider with the BISM signer domain.
- **No telemetry:** no analytics, crash-reporting or advertising SDKs.
- **Portal URLs:** the wallet links to `https://wallet.bismify.com` for terms,
  privacy, about and the download page.

Built from the wallet source branch `bism/task/BISM-WALLET-M19` @ `0486b6e`
(Flutter 3.44.0 / Dart 3.12.0), which is after the internal build tag
**BISM-WALLET-M14**. There was no separate public `v1.0.0` artifact before this
release, so this first public release already includes the post-M14 changes
(BISM-only selector, PIN/seed model, `bismify:` network id, rebranding).

### Assets

- `bism-wallet-v1.0.0.apk` — versioned APK
- `bism-wallet.apk` — stable-name copy (used by the `releases/latest/download` URL)
- `SHA256SUMS` — checksums
- `CHANGELOG.md` — this file
