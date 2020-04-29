# shadow-respawn

Minimalistic rustlang background app to automagically save and restore your opened apps on your Shadow VM, 
so it's less a pain when you get a shutdown and need to get back to the state you where in when you left.

## Features

For now I will focus the features described below:

**At start**

- [ ] check if already added to the Windows startup automatically
    - [ ] if not display a popup to ask if users wants automatic restore
- [ ] if a previous save has been detected :
    - [ ] if it contains a "> 20min idle" flag, restore all saved context
        - [ ] restart every unique processes
        - [ ] move and restore all windows to their previous states
        - [ ] do the same for every file explorer windows
    - [ ] if it doesn't contain a "> 20min idle" flag, prompt user if s.he wants to restore
- [x] otherwise :
    - [x] do nothing

**After start**

- [ ] list all running programs every minute
- [ ] save a list of all opened windows / processes (every minute)
    - [ ] save process name with fully qualified path
    - [ ] save each windows properties
        - [ ] save title
        - [ ] save coordinates
        - [ ] save dimensions
        - [ ] save state (maximized, minimized, normal)
- [ ] detect when user input has been missing for more than 20 minutes
- [ ] if so, add a "20min idle" flag in the file

**Miscellaneous**

- [ ] runs itself in the background as a Windows service or windowless app
- [ ] installs itself as a Windows service or autorun app at system startup
- [ ] allow setup of different timeouts for save and idle flag (defaults: 1min, 20min)
- [x] localized in English
- [ ] localized in French
- [ ] localized in German

*I'll probably never do the following ones... but they'd be nice !*

- [ ] restore all browser tabs and focus previously selected one if not restored by browser itself
- [ ] restore all opened files in common apps
    - [ ] MSOffice
    - [ ] Adobe Creative Cloud
- [ ] restore musics apps playlists to previously playing track


## Documentation

For now, no documentation, but the code should be pretty simple and self explanatory.

## Localization

Shadow has many users worldwide I know, so for now I only support English for faster dev,
but if you can provide help on that front, please ping me!

> **Et en français?** j'aurais bien aimé la langue de Molière qui m'est chère mais comme 
> il y a des utilisateurs de Shadow un peu partout je commence par l'anglais histoire que
> nos clients du monde entier soient pas trops perdus. 
>
> Promis, dès que j'ai du temps ou qu'un âme charitable se manifeste je mets du français :)

## Contribute

This is my first rustlang project, so feel free to contact me, any feedback and help welcome !
