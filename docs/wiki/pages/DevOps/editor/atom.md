# Editor > atom
[DevOps](../index.md) > [Editor](index.md)

## Overview
Atom is a text editor that's modern, approachable, yet hackable to the core -- a tool you can customize to do anything but also use productively without ever touching a config file.

https://atom.io/  
![atom-log](img/atom-log.png)

## Installation

### Install packages
```bash
$ apm install --package-file package.txt
```

* recommended packages writing in package.txt
```
autocomplete-modules
autocomplete-paths
build
gist-it
git-plus
gulp-control
highlight-selected
language-plantuml
language-powershell
markdown-preview-plus
merge-conflicts
minimap
minimap-autohide
minimap-bookmarks
minimap-highlight-selected
minimap-split-diff
mocha-test-runner
open-html-in-browser
open-recent
open-terminal-here
paste-table
plantuml-generator
plantuml-viewer
project-manager
script
split-diff
symbols-tree-view
test-status
todo-show
vim-mode-plus
vim-mode-plus-ex-mode
```

If you get list of packages that installed on your atom, execute blow .

```bash
$ apm list --installed --bare
```

note: you can share recommended package with checking stars on atom.io and can use stars package when installing.

```bash
$ apm stars --install
```

You can check the star to packages installed on your atom with using `apm star --installed`.

## Usage
### launch
```
$ cd path-to-project
$ atom .
```

### command pallete

#### operating files and folders

|short   |command       |command symbols        |
|--------|--------------|-----------------------|
|addfi   |add file      |tree view:add file     |
|addfo   |add folder    |tree view:add folder   |
|saval   |save all      |window:save all        |
|rename  |rename        |tree view:rename       |
|buffi   |buffer finder |Fuzzy Finder:Toggle Buffer Finder |
|gitfi   |git status finder|Fuzzy Finder:Toggle Git status Finder |

#### jump to symbol

|short   |command       |command symbols                   |
|--------|--------------|----------------------------------|
|fsymb   |file symbol   |symbols view:toggle file symbols  |
|decla   |declaration   |symbols view:Go to declaration    |
|retdecl |return form declaration|symbols view:return form declaration |

#### tab
|short         |command           |command symbols        |
|--------------|------------------|-----------------------|
|cntl+tab      |Show next item    |Pane:show next item    |
|cntl+shft+tab |Show previous item|Pane:show previou item |
|cntl+w        |close             |core:close             |


### snippet
You will have your own regularly-used code block which can be defined as snippets.
The snippet scope in snippets.cson must also hava a period added to the start of that string.

|type        |language scope   |
|------------|-----------------|
|Markdown    |.source.gfm      |
|javascript  |.source.js       |
|coffeescript|.source.coffee   |
|json        |.source.json     |
|cson        |.source.cson     |
|python      |.source.python   |
|ruby        |.text.html.erb   |
|java        |.source.java     |
|plain test  |.text.plain      |
|html        |.text.html.basic |
|css         |.source.css      |
|sass        |.source.sass     |

### shortcuts
|shortcuts   |command          |
|------------|-----------------|
|ctrl+shft+P |command pallet   |
|ctrl+shft+M |Markdown preview |
|ctrl+shft+B |run script       |
|F9          |run build (.atom-build.yml) |
|ctrl+alt+t  |terminal         |
|alt+shift+T |todo show        |

 - [ ] FIXME note using shortcuts

// --- end of file --- //
