% VIM_CHEAT_SHEET

Crashes
=======
- *vim -r* __file.swp__ : restore file

Files
=====
- *:w* __new_filename__ : save a copy and keep working on original

Moving around
=============
- *%* : move to matching item (__(__, __)__, __{__, __}__, __[__, __]__...)
- *g*/*G* : jump to end/beginning of __file__
- *0*/*$* : jump to end/beginning of __line__
- *H*/*M*/*L* : move to top/middle/bottom of the screen

Panels
======
- *(v)sp(lit)* : split screen (vertically)/horizontally

Tabs
====
- *vim -p* __{files}__
- *gt* : switch tab
- *tabf* __{file}__ : open file in new tab
- *tabdo* __{cmd}__ : run command through all tabs

BANG!
=====
Preffix by *:r* to paste the output.\
- *:r* __!__*ls*
- *:r* __!__*pwd*
- *:r* __!__*wc* __%__ (current file)


It can also be done after visually selecting some text : it is then piped to the cmd and replace the original content.\
- __!__*sort*


Formatting
==========
- *:=G* : indent file
- __\<select\>__+__{tabs count}__*>* : indent

Substitution
============
- *:%s/*__regex__*/*__replacement__*/g* : global find & replace

Navigation
==========
- *:*__{line number}__ : goto line
- */* __regex__ : search pattern
- *n*/*N* : next/previous

Insertion
=========
- __F2__ : 'set paste' mode
- *o*/*O* : insert mode on newline after/before current line

Copy-paste
==========
1. *v* : visual selection
2. *y*/*d* : copy (yank)/copy & delete
3. *p*/*P* : paste after/before
- *dd* : copy & delete line
- *yy* : copy line
- __["]__+__[+]__+__[Y]__ : copy line to system clipboard

Registers
=========
- __[0]__ : only populated with yanked text  __["]__+__[0]__+__[p]__
- __["]__ (default) : also populated with text from *d*/*x*/*c*/*s* commands

Commands
========
- *:*__[UP]__ : commands history
- *:u* : undo
- __[CTRL]+[R]__ : redo
- *:.* : repeat

Config
======
- *:verbose set* __var__*?* : get config value

Display
=======
- *:set list* : show special characters
- **^M** : Windows newline

More tips
=========
- *vimtutor*
