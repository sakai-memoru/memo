redmine
====

Overview
-----

Download
----- 
bitnami redmine download 
https://bitnami.com/stack/redmine

The Bitnami Redmine Stack provides a one-click install solution for Redmine by Bitnami.

* softwore stack
  - MySQL Database
  - Apache httpd
  - Redmine

Installation
------ 
1. Click installer that has downloaded.
 Select the installation language on English, so the installer can't display in Japanise.

2. Set admin account .
 The admin account will be used for Redmine and MySQL's root.

3. Set language for default data configuration on MySQL.
 Select your language for default data configuration on Japanese.

4. Configure SMTP Setting.

Usage
------ 
* After the installation, automatically kicked the services with bitnami navigation tool.  

![manage services](\img\bitnami-redmine-stack-ManageServers.JPG)

* Access to Redmine local site.
http://localhost/redmine

![first redmine site](\img\redmine-first-displayed.JPG)

* get started
  1. login admin with password that is set in the installation.
  2. Create user accounts.
  3. Create a Project, set tracker,ticket status, workflow, custome fields, enumulations.
  4. install plugins
     ex) \redmine\apps\redmine\htdocs\plugins

Installed environment
-----
Redmine 3.3.2.stable
Ruby 2.1.9-p490 (2016-03-30) [i386-mingw32]
Rails 4.2.7.1
Environment production
Database adapter Mysql2
git 2.10.2

Reference
-----
Windows版Bitnami Redmineをインストールする
http://qiita.com/ktyubeshi/items/64266d3c485b55869138
