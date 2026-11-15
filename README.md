# Bard releases

Published release files for [Bard: Clipboard, Draw and Dictate](https://github.com/miisodev/bard), the free, open-source clipboard, dictation and drawing companion for Windows and Linux.

[**Download**](https://miiso.dev/bard) · [Latest release](https://github.com/miisodev/bard-releases/releases/latest) · [Source](https://github.com/miisodev/bard) · [Speech models](https://github.com/miisodev/bard-models)

## What each release carries

| File | What it is |
| --- | --- |
| `Bard_<version>_x64-setup.exe`, `Bard_x64-setup.exe` | The Windows installer, versioned and under a stable name |
| `Bard_<version>_x64-setup.exe.sig`, `Bard_x64-setup.exe.sig` | Its Tauri updater signature |
| `latest.json` | The update manifest the Windows app reads through miiso.dev |
| `Bard_<version>_amd64.deb`, `Bard_amd64.deb` | The Debian and Ubuntu package |
| `Bard-<version>-1.x86_64.rpm`, `Bard_x86_64.rpm` | The Fedora and openSUSE package |
| `SHA256SUMS` | A checksum for every file above |
| `bard-sbom.json`, `bard-sbom-linux.json` | Software bills of materials |
| `release-provenance.json`, `release-provenance-linux.json` | The exact source commit and CI run each file was built from |

The stable names always point at the latest release, so `https://github.com/miisodev/bard-releases/releases/latest/download/Bard_x64-setup.exe` is a permanent download link.

## Verifying a download

Check the file against `SHA256SUMS` from the same release:

```sh
sha256sum --check --ignore-missing SHA256SUMS
```

The Windows installer is not Authenticode-signed, so SmartScreen warns the first time. Bard verifies every update's signature against the Ed25519 key built into the app before installing it; the provenance file names the source commit, tagged `vX.Y.Z` in [miisodev/bard](https://github.com/miisodev/bard), so you can build the same version yourself.

## Where things live

- **Source, issues and release notes:** [miisodev/bard](https://github.com/miisodev/bard)
- **Speech models:** [miisodev/bard-models](https://github.com/miisodev/bard-models)
- **Product page:** [miiso.dev/bard](https://miiso.dev/bard)

This repository holds release files only. Its own source archives contain this README and the licence, not Bard's code.

## License

[MIT](./LICENSE), the same as Bard.
