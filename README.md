# BISM Wallet — release binaries

This repository publishes **signed release binaries** for the **BISM Wallet**
Android application (`com.bismify.bism`). It contains **no source code** — only
release artifacts, their checksums, and this documentation.

- **Download page:** <https://wallet.bismify.com>
- **Latest APK:** <https://github.com/BismillahCoin/bism-releases/releases/latest/download/bism-wallet.apk>
- **All releases:** <https://github.com/BismillahCoin/bism-releases/releases>

The wallet source code is **not** public. BISM Wallet is a fork of the Auro
mobile wallet (Apache-2.0); the source remains in a private repository.

## Contents

| File | Purpose |
|---|---|
| Release assets (`bism-wallet*.apk`) | Signed Android packages |
| `SHA256SUMS` | SHA-256 checksums of the release assets |
| `CHANGELOG.md` | Release history |
| `LICENSE` | Apache-2.0 |

## Verify a download

Every release is signed with the same permanent BISM release certificate.

```bash
# 1. checksum
sha256sum -c SHA256SUMS            # macOS: shasum -a 256 -c SHA256SUMS

# 2. signer certificate
apksigner verify --verbose --print-certs bism-wallet.apk
#    or
keytool -printcert -jarfile bism-wallet.apk
```

Expected signer certificate SHA-256:

```
A4:24:13:2B:DC:FD:F7:17:17:EF:C8:74:DE:55:E4:75:24:6C:61:16:07:78:40:3D:C5:F1:FF:23:81:1E:E5:72
```

Expected package: `com.bismify.bism` · label: `BISM Wallet`.

If either check fails, **do not install** the file and report it via
<https://bismify.com>.

## Install

BISM Wallet is distributed as a signed APK (sideloading); it is not on Google
Play. See <https://wallet.bismify.com/install> for platform instructions.

## Security

- A self-custodial wallet never needs your seed phrase to "verify" anything.
  Never share your 24 words with anyone.
- Only download from this repository, <https://wallet.bismify.com>, or a
  published APKMirror/F-Droid listing.

## License

Apache-2.0 (see [LICENSE](LICENSE)). "Auro", "Mina" and "o1js" are third-party
marks; BISM is not affiliated with their owners.
