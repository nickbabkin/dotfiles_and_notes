% VIM_CHEAT_SHEET

Files
=====
- *:w* __new_filename__ : save a copy and keep working on original
- *vim -r* __file.swp__ : restore a file after a crash
- *vim -p* __{files}__ : open multiple files in tabs

Tabs
====
- *gt* : switch tab
- *tabf* __{file}__ : open file in new tab
- *tabdo* __{cmd}__ : run command through all tabs

Moving around
=============
- *%* : move to matching item (__(__, __)__, __{__, __}__, __[__, __]__...)
- *g*/*G* : jump to end/beginning of __file__
- *0*/*$* : jump to end/beginning of __line__
- *H*/*M*/*L* : move to top/middle/bottom of the screen

Panels
======
- *(v)sp(lit)* : split screen (vertically)/horizontally

BANG!
=====
Preffix by *:r* to paste the output.\
- *:r* __!__*ls*
- *:r* __!__*pwd*
- *:r* __!__*wc* __%__ (current file)
- *:cd* /path


It can also be done after visually selecting some text : it is then piped to the cmd and replace the original content.\
- __!__*sort*


Formatting
==========
- __\<leader\>__cc : comment toggle selection
- *guu*/*gUU*/*~* : lowercase line / uppercase line / invert case of selection
- __\<select\>__+__{tabs count}__*>* : indent
- *=* : auto (re)indent selection
- *=G* : auto (re)indent whole file

Substitution
============
- *:%s/*__regex__*/*__replacement__*/g* : global find & replace
- *:%g/*__regex__*/d* : delete all lines matching the pattern

Navigation
==========
- *:*__{line number}__ : goto line
- */* __regex__ : search pattern
- *n*/*N* : next/previous
- *\** : launch search with __regex__ = word under cursor

Insertion
=========
- __TAB__ : autocomplete ; use __TAB__+__SPACE__ for real tabs, and __TAB__+__TAB__ to cancel completion
- __F2__ : 'set paste' mode
- *o*/*O* : insert mode on newline after/before current line
- *:ci"* or *ci<* or *ci(* : delete everything on the line in-between "..."/<...>/(...) and enter insert mode

Copy-paste
==========
1. *v* : visual selection (or __CTRL__+V for vertical selection)
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
- *:.* : repeat last change - *:@* : repeat last command-line change

Config
======
- *:verbose set* __var__*?* : get config value
- *echo* os : get variable value

Display
=======
- **^M** : those are Windows newline
- *:set list* : show special characters
- *ga* : display ascii decimal, hex & octal value of character under cursor
- *:Ex* : file explorer (also __\<leader>__nn for NERDTree)
- *:ls* : list buffers (also __\<leader>__be for bufexplorer)

More tips
=========
- git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim && vim +PluginInstall +qall
- *:set spell* : enable vim 7.0+ spell checker
- *vimtutor*
- *ggg?G* : rot13 whole file
- :help!  - :help 42  - :help bar  -  :help holy-grail  -  :Ni! 
