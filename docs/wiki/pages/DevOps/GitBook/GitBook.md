[DevOps](../index.md) > [GitBook](index.md)

# GitBook

## Overview
* GitBook is a command tool for building beautiful book using GitHub/Git and markdown.
* You can publish and host books easily online using gitbook.com.
* Desktop tool is also available.

## Description

## Installation

``` powershell
> npm install gitbook-cli -g
```
### confirmation
``` powershell
> gitbook --version
```

### Initial Settings
``` powershell
> cd ~
> mkdir GitBook
> cd GitBook
> gitbook init
> ls
```
### Build the contents
``` powershell
> cd ~/GitBook
> gitbook build
```

### pubulish on localhost
``` powershell
> gitbook serve
```
* url : http://localhost:4000/

### Online publishing site
* url
  * https://www.gitbook.com/@sakai-memoru

### GitBook Editor
* url
  * https://www.gitbook.com/editor/osx
* 作成するmdファイルは、以下に保存される。
  * C:\Users\sakai\GitBook\Library\sakai-memoru\[book名]

## Usage
### Structure of GitBook
* 各フォルダごとに、文章の構造を管理する。
* フォルダの配下にファイルを作成する。
  * README.md   ・・・対象フォルダの説明(README)
  * SUMMARY.md  ・・・対象フォルダの目次の記述
* フォルダ配下に、サブフォルダも作成して同様の構造で、階層化できる。
```
.
├── README.md
├── index.md (mdwiki用)
├── SUMMARY.md
├── section-1
│   ├── README.md
│   ├── section-1-1.md
│   └── section-1-2.md
└── section-2.md
```

## How to use on first step
* N/A

## Reference
* GitBook
  * https://www.gitbook.com/about
* GitBookローカル開発環境セットアップ
  * https://qiita.com/mamohacy/items/98c0d790074c9bdfef1a

// --- end of file --- //
