# sic

A Command Line Password Manager Backed By GPG's Asymmetric Encryption

### Installation
```console
  curl -L https://raw.githubusercontent.com/aaoiki/sic/master/sic > ./sic && chmod +x ./sic
```

It's preferred to add the path to sic to your `PATH` variable
```console
  export PATH=$PATH:"/path/to/sic"
```

It's also recommended to add sic to your `HISTIGNORE` (or `HISTORY_IGNORE` for ZSH).

If you're using GPG 2.1.0+, you will see that GPG pops up a window asking for
the passphrase one more time after you've typed it in the command
line. This issue is reported [here](https://dev.gnupg.org/T1772). For me, I
added `pinentry-mode loopback` to gpg.conf and it stopped showing up.

### Usage
```console
$ sic h
NAME:
  sic - A Command Line Password Manager Backed By GPG's Asymmetric Encryption

USAGE:
  sic [options...] command [arguments...] [command options]

COMMANDS
  list, ls                           List all entries in the password store
  get, g          <key>              Get the value of a password entry. Pass the optional "-c" argument to copy the password to the clipboard
  add, a          <key> <value>      Add a password entry to the password store. To pass in a multi word value with spaces, wrap it in quotes
  edit, e         <key> <value>      Edit an existing entry
  remove, rm      <key>              Remove an existing entry
  help, h                            Show this message

OPTIONS
  -f      File to store passwords or set $SIC_FILE. Defaults to "~/.sic"
  -k      GPG keyid used for encryption & decryption or set $SIC_KEYID. Defaults to GPG's option "--default-key"
  -g      GPG used command or set $SIC_GPG. Defaults to "gpg2" then "gpg" if it was not found
  -y      Copying/yanking command or set $SIC_COPY. Defaults to "xclip -sel clip"
```

![sic GIF demo](/demo.gif)

### Similar Software
**sic** is highly inspired by:
- [pony](https://github.com/jessfraz/pony)
- [PASSBOX](https://github.com/RobBollons/passbox)

All credit goes to their authors.
