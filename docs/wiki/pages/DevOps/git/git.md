# Git > Git
[DevOps](../index.md) > [git](index.md)


## Overview
Git is a tool for tracking changes made to a set of files, known as a "version control system".You can use Git to track any kind of content at all.

## Description

## Installation

### Donwload
git for windows  
https://git-for-windows.github.io/

* git for windows provides a BASH emulation used to run Git from the command line.

### Installation
1. Install with download exe file.
2. Confirm setting in environment variables.
    ```powershell
    $ cmd
    $ powershell
    $ ($env:Path).split(';') | out-string -stream | select-string 'git'
    > // c:\Program files\git\cmd
    ```
3. check version
    ```cmd
    $ git --version
    > // git version 2.12.0.windows.1
    ```

## Usage at first step

### Set config
* Configure initial setting.
  ```powershell
    $ git config --global core.editor "vim"  ### set using editor
    $ git config --global user.name "sakai.memoru"
    $ git config --global user.email "sakai.memoru@gmail.com"
  ```
* see config
  ```powershell
    $ git config -l
  ```

* If you have proxy server in your network, set config below in addition.

  ```powershell
    $ git config --global http.proxy http://proxy.xxxx.co.jp:8080/
    $ git config --global https.proxy http://proxy.xxxx.co.jp:8080/
  ```

* If you configure difftool, set config blow.  
  Edit <$Home>\\.gitconfig
  ```ini
    [diff]
        tool = WinMerge
    [difftool "WinMerge"]
        path = c:/Program Files (x86)/WinMerge/WinMergeU.exe
        cmd = \"c:/Program Files (x86)/WinMerge/WinMergeU.exe\" -f \"*.*\" -e -u -r \"$LOCAL\" \"$REMOTE\"
    [merge]
        tool = WinMerge
    [mergetool "WinMerge"]
        path = c:/Program Files (x86)/WinMerge/WinMergeU.exe
        cmd = \"c:/Program Files (x86)/WinMerge/WinMergeU.exe\" -e -u \"$LOCAL\" \"$REMOTE\" \"$MERGED\"
    [alias]
        windiff = difftool -y -d -t WinMerge
        winmerge = mergetool -y -t WinMerge
  ```



### Case : Local repository only
* Create local repository
  ```powershell
    $ mkdir sample
    $ cd $$
    $ vim .gitconfig
    $ vim README.md
    $ git init     ### create and initialize git repository
    $ git add .    ### add all files to index area
    $ git status   ### display git working area status and index area status
    $ git commit -m 'first commit'  ### commit into local repository
    $ git status   ### display status
    $ git log      ### display commit logs
  ```

1. .gitconfig file

  ```text
    node_modules
    *.log
    *.*~
  ```

2. README.md

  ```markdown
    # sample
    ## Overview
    ## Description
    ## Demo
    ## Installation
    ## Usage
    ## Unit test
     :
  ```

### Case : Create Local repository connected to Shared Remote repository

* Create local repository with shared remote repository

  ```powershell
    $ mkdir sample
    $ cd $$
    $ vim .gitconfig
    $ vim README.md
    $ git init     ### create and initialize git repository
    $ git add .    ### add all files to index area
    $ git status   ### display git working area status and index area status
    $ git commit -m 'first commit'  ### commit into local repository
    $ git status   ### display status
    $ git log      ### display commit logs
    $ git remote add origin https://github.com/sakai-memoru/sample.git
    $ git push -u origin master
  ```

### Case : Clone Shared Remote repository

* Clone local repository connecting to shared remote repository

  ```powershell
    $ git clone https://github.com/sakai-memoru/sample.git
    $ cd <target directory:sample>
    $ vim .gitconfig
    $ vim README.md
    $ git add .    ### add all files to index area
    $ git status   ### display git working area status and index area status
    $ git commit -m 'commit messege'  ### commit into local repository
    $ git status   ### display status
    $ git log      ### display commit logs
    $ git push origin master
  ```

## Supplementals
### posh-git
- posh-git is a Powershell module that integrates Git and Powershell by providing Git status summary infomation that can be displayed in the powershell prompt.

  1. install psget

    ```powershell
      (new-object Net.WebClient).DownloadString("http://psget.net/GetPsGet.pa1") | invoke-expression
    ```
    Alternatively you can do installation manually.

  2. intall posh-git
    ```powershell
      Install-module posh-git -Startup
    ```

  3. On git repository directory , can use auto-complete git commands by using `tab` key

## Reference
私家版Git for Windowsのインストール手順  
https://opcdiary.net/?page_id=27065

git の差分比較・マージを WinMerge で行う  
http://qiita.com/kobake@github/items/fb317b4fdacad718a4b2

// --- end of file --- //
