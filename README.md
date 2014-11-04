mutt-office365
==============

A mutt configuration file ready for Office 365

## Preamble

Tested with Mutt 1.5.23 from source code.

Use your package manager to install Mutt.

You need Mutt >= 1.5.23 and the cyrus-sasl-plain package on RPM systems. If it is not available, follow these instructions:

```
# yum install gdbm-devel.x86_64 ncurses-devel.x86_64 cyrus-sasl-devel.x86_64 cyrus-sasl-plain.x86_64
# wget https://bitbucket.org/mutt/mutt/downloads/mutt-1.5.23.tar.gz
# tar xfvz mutt-1.5.23.tar.gz
# cd mutt-1.5.23
# ./configure --enable-debug --enable-imap --with-ssl --enable-smtp --enable-hcache --with-sasl
# make install
# ln -s /usr/local/bin/mutt /usr/bin/mutt
```

## Installation

Clone this repository into the `~/.mutt/` directory.

## Configuration

Edit the `~/.mutt/user` file.

```bash
# User config
set my_realname="John Smith"
set my_username="john.smith"
set my_domain="example.com"
set my_password="This password is secure"
set my_lang="fr_FR"
```

Don't forget your `~/.mutt/signature` file.
Contacts and mailing-lists are stored in `~/.mutt/aliases` and `~/.mutt/mailing_lists`.

## Usage

Key bindings are used to move across IMAP folders. Sent messages are placed in
the adequate folder. The IMAP connexion is persistent, thus making folders up to date without
any user intervention.

The new commands:
```
gi : Go to the inbox
gs : Go to the sent messages
gt : Go to the trash
gd : Go to the drafts
G  : Force IMAP sync
```

## Todo

Office365 IMAP folders are localized, which means we have to create dedicated config
files for each language. Language definitions are placed under the `.mutt/lang/`
directory.

Feel free to send me a pull request with the changes for your language.
