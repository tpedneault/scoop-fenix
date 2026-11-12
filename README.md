# scoop-fenix

The [Scoop](https://scoop.sh) bucket for [Fenix](https://github.com/tpedneault/fenix),
the keyboard-first text editor.

```powershell
scoop bucket add fenix https://github.com/tpedneault/scoop-fenix
scoop install fenix
```

`scoop update fenix` brings a newer release. The manifest follows Fenix's
releases by itself: a scheduled workflow checks for a new one every day
and updates `bucket/fenix.json`.

## The nightly

`fenix-nightly` is Fenix's
[nightly build](https://github.com/tpedneault/fenix/releases/tag/nightly):
`master`, built each night it changed. It isn't a release
([what that means](https://github.com/tpedneault/fenix/blob/master/docs/RELEASING.md#for-users-running-the-nightly)).

```powershell
scoop install fenix-nightly
```

`scoop update fenix-nightly` brings the newest one; `fenix --version`
says which you have and the commit it was built from. The same workflow
keeps `bucket/fenix-nightly.json` at the latest nightly, version and
hash. In the hours between a nightly being published and the manifest
catching up, an install or update fails on the hash: `scoop update` and
try again later.

It can be installed beside `fenix`. Both provide the `fenix` command,
which is the one installed last; `scoop reset fenix` or
`scoop reset fenix-nightly` picks the other. They share your settings.

Fenix is also available as a Windows installer, and as .deb and .rpm packages; see its
[install instructions](https://github.com/tpedneault/fenix#install).
