Memo
==============

Publish markdown files with mdwiki , and host on github site.  
https://sakai-memoru.github.io/memo/docs/

If you review making site on local pc, change directory into docs directory and execute http-server.Then access url blow.

* local access url  
http://localhost:8081/

![http-server-execution](img/http-server-execution.jpg)


* Http-server Installation
  ```bash
  $ npm install http-server -g
  ```

* .atom-build.yml
Install build package on atom, execute build with F9 shortcut.
```yml
cmd : http-server
```


// --- end of file --- //
