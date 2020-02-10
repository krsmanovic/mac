## Offline MAC address finder

Are you tired of going online every time you need to search OUI database? Introducing: offline MAC address finder, a simple bash utility doing just that - but on your Linux machine.

## Installation

First make sure that `/usr/local/bin` is in your $PATH and then download `bash` files to your machine:

```
sudo wget -O /etc/cron.monthly/oui https://raw.githubusercontent.com/krsmanovic/mac/master/oui
sudo wget -O /usr/local/bin/mac https://raw.githubusercontent.com/krsmanovic/mac/master/mac
```
Then make cron job execjutable and run it once in order to download IEEE MAC address database:

```
sudo chmod +x /etc/cron.monthly/oui
sudo /etc/cron.monthly/oui
```
This way database is updated once a month. :)

## Usage instructions

Simply type `mac` without parameters and enter the MAC at the prompt:

```
mac
```
or
```
mac ADDRESS
```
where `ADDRESS` is either whole or partial (at least 6 characters), formatted in any way you got.
