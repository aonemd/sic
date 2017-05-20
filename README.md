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
  add, a          <key> <value>      Add a password entry to the password store
  edit, e         <key> <value>      Edit an existing entry
  remove, rm      <key>              Remove an existing entry
  help, h                            Show this message

OPTIONS
  -f      File to store passwords or set $SIC_FILE. Defaults to "~/.sic"
  -k      GPG keyid used for encryption & decryption or set $SIC_KEYID. Defaults to GPG's option "--default-recipient-self"
  -e      GPG used command or set $SIC_GPG. Defaults to "gpg2" then "gpg" if it was not found
  -y      Copying/yanking command or set $SIC_COPY. Defaults to "xclip -sel clip"
```

### Similar Software
**sic** is highly inspired by:
- [pony](https://github.com/jessfraz/pony)
- [PASSBOX](https://github.com/RobBollons/passbox)
- [pwd.sh](https://github.com/drduh/pwd.sh)

All credeit goes to their authors.
