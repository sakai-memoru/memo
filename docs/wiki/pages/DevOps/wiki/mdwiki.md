# Wiki > mdWiki

[DevOps](../index.md) > [wiki](index.md)

## Overview
Expose markdown files on GITHUB.

Can use docs directory.See below url.  
[wiki](index.md) > [hosted-pages-on-github](./hosted-pages-on-github.md)

Click link for markdown.  
[wiki](index.md) > [markdown](./markdown.md)

- [ ] TODO : Create JSDoc into docs folder.

## Description

MDWiki is a Wiki completely built in only HTML5/javascript and runs 100% on the client.  
MDwiki can be hosted through GitHub.
http://dynalon.github.io/mdwiki/#!index.md
http://dynalon.github.io/mdwiki/#!tutorials/github.md

* Step1
  - Get a GitHub account.
* Step2
  - Fork mdwiki-seed or clone it.

```bash
$ git clone https://github.com/exalted/mdwiki-seed.git
$ cd mdwiki-seed
$ git remote add wiki <clone url of the new repository>
$ git push wiki gh-pages
```

* Step3
  - Custmize sites

## Note
It all begins by creating an initial file structure for any language that you would like to support. You will duplicate `ll_cc` folder and rename your copy to `wiki`.

`ll_cc` is a starter template folder which you should't ever edit directory, since you may loose your changes when MDwiki gets updated later.

## Getting started
Suppose your first wiki is going to be in Japaniese, hence you must have a folder called `wiki`, as reviously described.

1. Open `index.html` file.
2. Find where it says "override `ll_cc` below with your default path "
3. Change refresh meta tag from `url=ll_cc/` to `url=wiki/`. (trailing `/` is very imortant)

## MDWiki's more detail

### How does MDWiki Work?
You just download the mdwiki.html available form the download page along with your markdown files on a webspace somewhere. You can pass any url (relative to the mdwiki.html file) to mdwiki after the hashbang `#!`.

```
http://localhost/mdwiki.html#!README.md
```

If you rename the `mdwiki.html` into `index.html` , you can omit the filename on most web servers.

```
http://localhost/#!README.md
```
MDWiki will load a file called `index.md` from the same directory as the index.html by default, so if you use an `index.md` file as entry point, all you have to do is enter your domain name.

```
http://localhost/
```


note: site of quick start.  http://dynalon.github.io/mdwiki/#!quickstart.md

### Adding a navigation

Create a navigation.md file in  the same directory as the mdwiki.html and put in the links that make up your menu.

```
# wiki
[About](about.md)
[Download](download.md)
[links](links.md)
```
For more comple menus , nesting submenu items as a list and using horizontal lines that will be rendered as dividers is also possible.

```
# wiki
[About](about.md)
[Download](download.md)
[DevOps](pages/devops)
  * [MDWiki](pages/devops/mdwiki/)

[links](links.md)
[gimmick:themechooser](Choose theme)
[gimmick:theme](cosmo)
```

### Gimmicks

Through the usage of Gimmicks, which are like plugins, you can add much more dynamic elements into your wiki and use it in a very advanced way.

http://dynalon.github.io/mdwiki/#!quickstart.md

* Alert

|type   |trigger          |
|-------|-----------------|
|Warning|warning,attention|
|Note   |note             |
|Hint   |hint,tip         |

* Gist
```
[gimmick:gist](5641564)
```
Preview:
[gimmick:gist](5641564)

- [ ] TODO update `gimmicks/gist.js` revision ,that will apply for alphanumeric gist id.

* UML Diagrams via yUML.me
http://yuml.me/

```
[gimmick:yuml]([HttpContext]uses -.-> [Reponse])
```

[gimmick:yuml]([HttpContext]uses -.-> [Reponse])

* Disqus

Adds comment to your website. You first need to sign up with disqus and use your disqus short name as the link target.

```
[gimmick:Disqus](disqus-account)
```

[gimmick:Disqus](memorusakai)

- [ ] FIXME implement `gimmicks/disqus.js` correctly.

// --- end of file --- //
