# OGVault releases

This repository only holds the release files of OGVault, a local password manager for Windows.
There is no source code here.

Each release has three files:

- `OGVault.exe`: the app.
- `latest.json`: the version number, the exe's size and its SHA-256 fingerprint, and a short note
  about what changed.
- `THIRD_PARTY_LICENSES.txt`: the licences of the open-source parts OGVault is built with.

## How OGVault uses it

From version 1.0.2 on, OGVault asks this repository once a day whether a newer version exists (you can
turn that off in Settings → Updates, or check by hand there). It only reads
`releases/latest/download/latest.json` and, when you click **Update now**, downloads `OGVault.exe` from
the matching release. Before replacing itself it checks that the download has exactly the size and
SHA-256 written in `latest.json`, and it never installs an older or the same version. Nothing about
you or your vault is sent.

## Updating by hand

Download `OGVault.exe` from the latest release and put it in place of your old one. Your vault and
settings are stored separately, so they stay as they are.

## If OGVault doesn't open after an update

The update keeps the previous version next to the new one, as `OGVault.exe.old`, until the new
version has started. If the new version doesn't open:

1. Close OGVault if it is still running.
2. In File Explorer, turn on **View → Show → File name extensions** (on Windows 10, **View →
   File name extensions**). Without it, Explorer shows `OGVault.exe` as just `OGVault`, and
   `OGVault.exe.old` as `OGVault.exe`.
3. In the folder with OGVault, delete `OGVault.exe`.
4. Rename `OGVault.exe.old` to `OGVault.exe`. If Windows warns that changing the extension may
   make the file unusable, click **Yes**.
5. Open OGVault as usual. Your vault and settings are untouched.
