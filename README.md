**Setup**
Install pass cli and clone this repository to ~/.password-store
```
brew install pass
git clone git@github.com:benchacko/pass.git ~/.password-store
```

Import encryption key and set trust
```
gpg --import private.pgp
gpg --list-keys
gpg --edit-key XXXXXXXXXXXXXXX
gpg (GnuPG) 2.4.8; Copyright (C) 2025 g10 Code GmbH
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Secret key is available.
.
.
.
gpg> trust
.
.
.
Please decide how far you trust this user to correctly verify other users' keys
(by looking at passports, checking fingerprints from different sources, etc.)

  1 = I don't know or won't say
  2 = I do NOT trust
  3 = I trust marginally
  4 = I trust fully
  5 = I trust ultimately
  m = back to the main menu

Your decision? 5
Do you really want to set this key to ultimate trust? (y/N) y
.
.
.
Please note that the shown key validity is not necessarily correct
unless you restart the program.

gpg> exit
```
