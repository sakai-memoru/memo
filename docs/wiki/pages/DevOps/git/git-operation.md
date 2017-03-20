# Git > git-operation
[DevOps](../index.md) > [git](index.md)

## Overview
git operation

- [ ] FIXME : What happen on using git ?

## Description
### git commit --amend

```bash
$ git commit --amend
```

### git reset --soft HEAD^
直前のcommtを、取り消す。working-tree,indexはそのまま。
```bash
$ git reset --soft HEAD^
```
```bash
$ git reset --soft @^
```


### git rm --cached

```bash
$ git rm --cashed
$ vim .gitignore
```

### git rebase -i HEAD^3

```bash
$ git rebase -i HEAD^3
```

Before modifying
```
pick aa11bbc message1
pick bb22dde message2
pick cc33ffg message3
```
After
```
pick aa11bbc message1
squash bb22dde message2
squash cc33ffg message3
```
cf) fixup

### git reset --hard HEAD
Reset working tree and index and restore HEAD.
```bash
$ git reset --hard HEAD
```

### git reset --hard HEAD^
直前のコミットを取り消す。Clear working-tree and index.
```bash
$ git reset --hard HEAD^
```

### git reset HEAD
addを取り消す。Clear index.
```bash
$ git reset HEAD
```
```bash
$ git reset --mixed HEAD
```

## Add empty directory
You can not add the directory that has no files to repository. create a file named .gitkeep in the structured directories.

// --- end of file --- //
