mutt-office365
==============

A mutt configuration file ready for Office 365

## Installation

Clone this repository into the `~/.mutt/` directory.

## Configuration

Edit the `~/.mutt/muttrc` file.

```bash
# User config
set my_realname="John Smith"
set my_username="john.smith"
set my_domain="example.com"
set my_password="This password is secure"
set my_lang="fr_FR"
```

Don't forget your `~/.mutt/signature` file.

## Todo

Office365 IMAP folders are localized, which means we have to create dedicated config
files for each language. Language definitions are localized under the `.mutt/lang/`
directory.

Feel free to send me a pull request with the changes for your language.
