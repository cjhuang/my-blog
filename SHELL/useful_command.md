# Some Useful Shell Command #
-------

## watch ##
execute a program periodically, showing output fullscreen

## alsamixer ##
soundcard mixer for ALSA soundcard driver, with ncurses interface

## xlsfonts ##
server font list displayer for X

## rsync ##
a fast, versatile, remote (and local) file-copying tool

## apt-get source ##
get the source of soft

## dircolors ##
color setup for ls

We can export the default setting using 'dircolors -p' to file, eg.
.lscolors, the use the command 'eval \'`dircolors -b $HOME/.lscolor`\' in
.bashrc before alias ls to
use the your own setting. In file \".lscolor\", you can set arbitrary color
for any file.

## pdftk ##
Editor pdf, e.g. break up, merge, rotate and so on.

## cron ##
daemon to execute scheduled commands
> crontab -u user -e
