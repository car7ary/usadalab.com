# MX Linux

## .bash_profileが読み込まれない

Lightdmは起動時に`.bash_profile`を読み込まないようなので`.xsessionrc`に設定を追加する。

```bash
# .xsessionrc
. ${HOME}/.bash_profile
```

