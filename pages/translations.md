---
title: 08. Translations
permalink: translations.html
---

# Translations
Our stack comes with POT file generator utility. Please follow the steps below to generate POT file
for your theme and mu-plugin. 

### Prerequisites
In order to generate translations files you need to have `xgettext` utility available on your environment.

On **MacOS** you can install it via `homebrew`:
```
brew install gettext
brew link gettext --force
```
In case you have conflicts with built in BSD version of xgettext you should unlink your homebrew one.


### Running the generator
Generator and its configuration can be found in `/RaccoonWP/utils` directory. 
If you need to adjust it please edit the `.sh` file.

In order to generate .pot files please navigate to project root and run following command in your terminal
```
composer run-script make-pot
```

After .pot files are generated you can use any tool (for example [Poedit](https://poedit.net/)) to generate your language .po and .mo files.


