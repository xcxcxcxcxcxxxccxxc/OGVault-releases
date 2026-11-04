# OGVault releases

This repository only holds the release files of OGVault, a local password manager for Windows.
There is no source code here.

Each release has two files:

- `OGVault.exe`: the app.
- `latest.json`: the version number, the exe's size and its SHA-256 fingerprint, and a short note
  about what changed.

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
