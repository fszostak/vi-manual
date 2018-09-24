VI Editor Manual 
===================
<small>Initial version 2004 by Fabio Szostak, updated 2018</small>


VI editor command summary. Enjoy and increase it. You're welcome.

----------

**Open, save and exit**

On shell:

```
$ vi filename
```

On editor:<br/>
<br/>
**:e filename** open file<br/>
**:e! filename** open file with ignore changes<br/>
**:e#** *or* **:e!#** open previous file<br/>
**:wq** *or* **:x** *or* **:x!** save and exit<br/>
**:q!**  exit without save<br/>
<br/>
**!!command**  run *command* and get output<br/>
<br/>
Check on bottom of screen the command mode:<br/>
<br/>
**nothing** is on *command* mode<br/>
**-- INSERT --**  is on *insert* mode<br/>
**-- REPLACE --**  is on *replace* mode<br/>
<br/>
Note: Always type <kbd>esc</kbd> to switch to command mode<br/>

<table width="0">
<tr>
<td valign="top">

*Basic commands*

**Navigation**

<kbd>h</kbd> go left, like <kbd>&larr;</kbd> <br/>
<kbd>j</kbd> go down, like <kbd>&darr;</kbd><br/>
<kbd>k</kbd> go up, like <kbd>&uarr;</kbd><br/>
<kbd>l</kbd> go right, like <kbd>&rarr;</kbd><br/>
<kbd>0</kbd> begin of line<br/>
<kbd>$</kbd> end of line<br/>
<kbd>H</kbd> top of screen<br/>
<kbd>L</kbd> bottom of scree**n**<br/>
<kbd>w</kbd> begin next word<br/>
<kbd>e</kbd> end next word<br/>
<kbd>b</kbd> back previous word<br/>
<kbd>CTRL-F</kbd> go next page, like <kbd>PageDown</kbd><br/>
<kbd>CTRL-B</kbd> go previous page, like <kbd>PageUp</kbd><br/>
<kbd>G</kbd>  go end of file<br/>
**:n** go to line number <br/>
**:$** go to end of file<br/>

**Search**

<kbd>/</kbd> *+* **str**  find next match *str*<br/>
<kbd>?</kbd> *+* **str**  find previous match *str*<br/>
<kbd>%</kbd> find match close char {}()[]<br/>

**Insert mode**
 
<kbd>i</kbd>  enter on insert mode<br/>
<kbd>I</kbd>  at begin of line<br/>
<kbd>a</kbd>  at next character<br/>
<kbd>A</kbd>  at end of file<br/>
<kbd>o</kbd>  at next line<br/>
<kbd>O</kbd>  at previous line<br/>

**Undo changes**

<kbd>u</kbd>  last command<br/>
<kbd>U</kbd>  all commands in current line<br/>

**Delete**

<kbd>x</kbd>  delete current character<br/>
<kbd>dd</kbd>  delete current line<br/>
**:g/regexp/d**  delete all lines match *regexp*<br/>

**Replace mode**

<kbd>r</kbd>   replace one character <br/>
<kbd>R</kbd>   enter in replace mode<br/>
<kbd>cw</kbd>  replace current word<br/>
<kbd>s</kbd>  replace one char and enter in replace mode<br/>
<br/>
**:x,y s /find/replace/g**  find and replace<br/>
*x,y* is line range, *%* is oll, *g* is all occurences in line<br/>
<br/>
<kbd>~</kbd>  change character case (uppercase|lowercase)<br/>

**Join lines**

<kbd>J</kbd>  Join current line with next line<br/>

**Repeat**

<kbd>.</kbd>  Repeat last command<br/>

**Indent**

<kbd>>></kbd> shift current line to right<br/>
<kbd><<</kbd> shift current line to left<br/>

**Put to buffer**

<kbd>yy</kbd> *or* <kbd>Y</kbd> put current line to temporary buffer<br/>

**Paste buffer**

<kbd>P</kbd> paste buffer previous line<br/>
<kbd>p</kbd> paste buffer next line<br/>

**Mark**

<kbd>m</kbd>**[a-z]** put *[a-z]* mark in current line<br/>
<kbd>’</kbd>**[a-z]** go to *[a-z]* mark<br/>
<kbd>’’</kbd> go to last mark<br/>

</td>
<td valign="top">

*Advanced commands*

**Navigation**

**n** <kbd>h</kbd> go *n* chars to left <br/>
**n** <kbd>j</kbd> go *n* lines to down<br/>
**n** <kbd>k</kbd> go *n* lines to up<br/>
**n** <kbd>l</kbd> go *n* chars to right<br/>

**n** <kbd>w</kbd> go next *n* words<br/>
**n** <kbd>e</kbd> go next *n* words at end<br/>
**n** <kbd>b</kbd> go back *n* words<br/>

**n** <kbd>G</kbd> go *n* lines from begin of file<br/>

**Insert mode**

**n** <kbd>i</kbd> insert **n** times after <kbd>esc</kbd><br/>
**n** <kbd>I</kbd> insert **n** times after <kbd>esc</kbd><br/>
**n** <kbd>a</kbd> insert **n** times after <kbd>esc</kbd><br/>
**n** <kbd>A</kbd> insert **n** times after <kbd>esc</kbd><br/>

**Delete**

**n** <kbd>x</kbd> delete *n* characters<br/>
**n** <kbd>dd</kbd> delete *n* lines<br/>
<kbd>d/</kbd> **str** delete until match *str*<br/>
<kbd>d%</kbd> delete match character {}[]()<br/>
<kbd>dG</kbd> delete until end of file<br/>
<kbd>d1G</kbd> delete to beginning of file<br/>
<kbd>d</kbd> **n** <kbd>G</kbd> delete to beginning of file, except *n* first lines<br/>
<kbd>dw</kbd> delete to end of word<br/>
<kbd>d</kbd> **n** <kbd>w</kbd> delete **n** words<br/>

**Replace mode**

**n** <kbd>s</kbd> replace **n** characters<br/>
<kbd>c</kbd> **n** <kbd>w</kbd> replace *n* words<br/>
<kbd>c$</kbd> replace to end of line<br/>
<kbd>c0</kbd> replace to beginning of line<br/>
<kbd>c/</kbd> **str** replace until match *str*<br/>
<kbd>c%</kbd> replace to match char {}[]()<br/>
<kbd>cG</kbd> replace to end of file<br/>

**Join lines**

n<kbd>J</kbd> **n**  join **n* lines above current line<br/>

**Indent**

**n** <kbd>>></kbd>  shift *n* lines to right<br/>
**n** <kbd><<</kbd>  shift *n* lines to left<br/>
<kbd>>%</kbd> shift until match char to right<br/>
<kbd><%</kbd> shift until match char to left<br/>
<kbd>>G</kbd> shift to end of file<br/>
<kbd>>1G</kbd> shift to beginning of file<br/>
<kbd>>/</kbd> **str** shift until match *str*<br/>

**Registers**

<kbd>“</kbd> **[a-z]** open the register<br/>
<kbd>@</kbd> **[a-z]** execute commands into the register <br/>

**Put to register**

<kbd>“</kbd> **r** <kbd>yy</kbd>  put current line to register “r”<br/>
<kbd>“</kbd> **r** <kbd>y’</kbd> **m**  put until match mark "m” to register "r"<br/>
<kbd>“</kbd> **r** <kbd>y/</kbd> **str**  put until find string *"str"* to register *"r"*<br/>
<kbd>“</kbd> **r** <kbd>y$</kbd> put until find end of line to register *"r"*<br/>
<kbd>“</kbd> **r** <kbd>yw</kbd> put one word to register *“r”*<br/>

**Get from register**

<kbd>“</kbd> **r** <kbd>p</kbd> paste content of register “r” after<br/>
<kbd>“</kbd> **r** <kbd>P</kbd> paste content of register “r” before<br/>

</td>
</tr>
</table>


**RegExp Replace Example**


```
 ORIGINAL FILE         CHANGED FILE
 ........ 1234.10  =>  ........ 1234,10
 ........ 2233.20  =>  ........ 2233,20 

Command:       :1,$ s /\.\([0-9]\)/,\1/

Find:     .(dígit 0 to 9)
Replace:  ,(dígit 0 to 9)
```
<br/>
