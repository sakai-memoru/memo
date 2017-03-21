# Editor > vim
[DevOps](../index.md) > [Editor](index.md)

## Overview
Vim ; a contraction of Vi IMproved, is a clone a done of vi text editor.

KaoriYa VIM  
https://www.kaoriya.net/software/vim/

- [ ] TODO : Note vim operations , comment in/out, indent/deindent,...

## Description

## Installation

## Usage

### Change mode
|key      |operation            |
|---------|---------------------|
|esc      |normal mode          |
|aiosc    |insert mode          |
|v        |visual mode          |
|:        |command mode         |

### normal mode
#### operation

|key      |operation            |
|---------|---------------------|
|x        |delete charactor     |
|r        |replace charactor    |
|R        |replace charactor    |
|~        |upper/lowercase charactor|
|c<motion>|cw                   |
|C        |c$                   |
|d<motion>|dw, d$               |
|D        |d$                   |
|ia       |insert,add           |
|IA       |insert first,add last|
|s        |delete and insert    |
|yy       |yank line            |
|dd       |delete line          |
|cc       |delete line and insert  |
|S        |delete line and insert  |
|J        |join line            |
|oO       |insert line          |
|pP       |paste                |
|---------|---------------------|
|.        |repeat               |
|u,ctrl+Z |undo                 |

#### motion
|key  |operation            |
|-----|---------------------|
|w/b  |word                 |
|fx   |search 'x'word       |
|tx   |search until 'x'word |
|1l   |n time hjkl          |

#### jump
|key  |operation            |
|-----|---------------------|
|hjkl |move cursor          |
|wW   |move forward word    |
|eE   |move forward word    |
|bB   |move back word       |
|]}   |move forward block   |
|[{   |move back block      |
|%    |move to another bracket |
|gg   |jump to top          |
|G    |jump to bottom       |
|*    |jump to word above cursor |
|/hoge|jump to search word  |
|n/N  |jump next word       |

#### command

|key  |operation       |
|-----|----------------|
|:w   |write           |
|:q   |quit            |
|:e   |edit other file |

#### scroll
|key  |operation            |
|-----|---------------------|
|HML  |windows high/middle/low   |
|ctrl+u/d |windows up/down       |

### insert mode


// --- end of file --- //
