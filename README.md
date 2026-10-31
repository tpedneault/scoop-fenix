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

Fenix is also available as a Windows installer and on winget; see its
[install instructions](https://github.com/tpedneault/fenix#install).
