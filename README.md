VI - Manual by Fabio Szostak!
===================


VI command summary. Enjoy and increase it. You're welcome.

----------

<table width="0">
<tr>
<td valign="top">

*Basic commands*

**Edition**

**:e filename** open file<br/>
**:e! filename** open file with ignore changes<br/>
**:e#** *or* **:e!#** open previous file<br/>
**:wq** *or* **:x** *or* **:x!** save and exit<br/>
**!!command**  run *command* and get output<br/>

**Navigation**

<kbd>h</kbd> like <kbd>&larr;</kbd> <br/>
<kbd>j</kbd> like <kbd>&darr;</kbd><br/>
<kbd>k</kbd> like <kbd>&uarr;</kbd><br/>
<kbd>l</kbd> like <kbd>&rarr;</kbd><br/>
<kbd>0</kbd> begin of line<br/>
<kbd>$</kbd> end of line<br/>
<kbd>H</kbd> top of scree**n**<br/>
<kbd>L</kbd> bottom of scree**n**<br/>
<kbd>w</kbd> begin next word<br/>
<kbd>e</kbd> end next word<br/>
<kbd>b</kbd> back previous word<br/>
<kbd>CTRL-F</kbd> like <kbd>PageDown</kbd><br/>
<kbd>CTRL-B</kbd> like <kbd>PageUp</kbd><br/>
<kbd>G</kbd>  go end of file<br/>
**:n** go to line number <br/>
**:$** go to end of file<br/>

**Search**

<kbd>/</kbd> str find next match<br/>
<kbd>?</kbd> str find previous match<br/>
<kbd>%</kbd> find match close char {}()[]<br/>

**Insert**
 
<kbd>i</kbd>  enter in insert mode<br/>
<kbd>I</kbd>  enter insert mode at begin of line<br/>
<kbd>a</kbd>  at next character<br/>
<kbd>A</kbd>  enter insert mode at end of file<br/>
<kbd>o</kbd>  enter insert mode at next line<br/>
<kbd>O</kbd>  enter insert mode at previous line<br/>

**Undo changes**

<kbd>u</kbd>  last command<br/>
<kbd>U</kbd>  all commands in current line<br/>

**Delete**

<kbd>x</kbd>  delete current character<br/>
<kbd>d</kbd> *+* <kbd>d</kbd>  delete current line<br/>
**:g/regexp/d** delete all lines match regexp<br/>

**Replace mode**

<kbd>r</kbd>   replace one character <br/>
<kbd>R</kbd>   enter in replace mode<br/>
<kbd>c</kbd>+<kbd>w</kbd>  replace current word<br/>
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

<kbd>></kbd><kbd>></kbd> shift current line to right<br/>
<kbd><</kbd><kdb><</kbd> shift current line to left<br/>

**Copy to buffer**

<kbd>y</kbd> *+* <kbd>y</kbd> copy current line to temporary buffer<br/>
<kbd>Y</kbd> copy current line to temporary buffer<br/>

**Paste buffer**

<kbd>P</kbd> paster buffer previous<br/>
<kbd>p</kbd> paste buffer next<br/>

**Mark**

<kbd>m</kbd>**[a-z]** put *[a-z]* mark in current line<br/>
<kbd>’</kbd>**[a-z]** go to *[a-z]* mark<br/>
<kbd>’</kbd> *+* <kbd>’</kbd> go to last mark<br/>

</td>
<td valign="top">

*Advanced commands*

**Navigation**

**n**<kbd>h</kbd> **n** chars to left <br/>
**n**<kbd>j</kbd> **n** lines to dow**n**<br/>
**n**<kbd>k</kbd> **n** lines to up<br/>
**n**<kbd>l</kbd> **n** chars to right<br/>

**n**<kbd>w</kbd> **n** words<br/>
**n**<kbd>e</kbd> **n** words<br/>
**n**<kbd>b</kbd> back **n** words<br/>

**n**<kbd>G</kbd> **n** lines from begin of file<br/>

**Insert mode**

**n**<kbd>i</kbd> insert **n** times <br/>
**n**<kbd>I</kbd> insert **n** times <br/>
**n**<kbd>a</kbd> insert **n** times <br/>
**n**<kbd>A</kbd> insert **n** times <br/>

**Delete**

**n**<kbd>x</kbd> **n** characters<br/>
**n**<kbd>d</kbd> *+* <kbd>d</kbd> **n** lines<br/>
<kbd>d</kbd>/str até encontrar str<br/>
<kbd>d</kbd><kbd>%</kbd> delete to match character {}[]()<br/>
<kbd>d</kbd><kbd>G</kbd> delete to end of file<br/>
<kbd>d</kbd><kbd>1</kbd>G</kbd> delete to begining of file<br/>
<kbd>d</kbd>n<kbd>>G</kbd> delete to begining of file, except **n** first lines<br/>
<kbd>d</kbd><kbd>w</kbd> delete to end of word<br/>
<kbd>d</kbd>n<kbd>>w</kbd> delete **n** words<br/>

**Replace mode**

**n**<kbd>s</kbd> **n** characters<br/>
<kbd>c</kbd>**n**<kbd>w</kbd> **n** words<br/>
<kbd>c</kbd><kbd>$</kbd> replace to end of line<br/>
<kbd>c</kbd><kbd>0</kbd> replace to beginning of line<br/>
<kbd>c</kbd><kbd>/</kbd>str replace to match *str*<br/>
<kbd>c</kbd><kbd>%</kbd> replace to match char {}[]()<br/>
<kbd>c</kbd><kbd>G</kbd> replace to end of file<br/>

**Join lines**

nJ **n** join **n* lines above current line<br/>

**Indent**

**n**<kbd>></kbd><kbd>></kbd> *n* lines to right<br/>
**n**<kbd><</kbd><kbd><</kbd> *n* lines to left<br/>
<kbd>></kbd><kbd>%</kbd> shift match char to right<br/>
<kbd><</kbd><kbd>%</kbd> shift match char to left<br/>
<kbd>></kbd><kbd>G</kbd> shift to end of file<br/>
<kbd>>1</kbd><kbd>G</kbd> shift to beginning of file<br/>
<kbd>></kbd><kbd>/</kbd>**str** shift to match *str*<br/>

**Registers**

<kbd>“</kbd>**[a-z]** open the register<br/>
<kbd>@</kbd>**[a-z]** execute commands into the register <br/>

**Put to register**

<kbd>“</kbd>**r**<kbd>y</kbd><kbd>y</kbd>  put current line to register “r”<br/>
<kbd>“</kbd>**r**<kbd>y</kbd><kbd>’</kbd>**m**  put until match mark "m” to register "r"<br/>
<kbd>“</kbd>**r**<kbd>y</kbd><kbd>/</kbd>**str**  put until find string *"str"* to register *"r"*<br/>
<kbd>“</kbd>**r**<kbd>y</kbd>$</kbd> put until find end of line to register *"r"*<br/>
<kbd>“</kbd>**r**<kbd>y</kbd><kbd>w</kbd> put one word to register *“r”*<br/>

**Get from register**

<kbd>“</kbd> *+* **r** *+* <kbd>p</kbd> paste content of register “r” after<br/>
<kbd>“</kbd> *+* **r** *+* <kbd>P</kbd> paste content of register “r” before<br/>

</td>
</tr>
</table>


**RegExp Example**

 ORIGINAL FILE         CHANGED FILE<br/>
 ........ 1234.10  =>  ........ 1234,10 <br/>
 ........ 2233.20  =>  ........ 2233,20 <br/>
<br/>
Command:       :1,$ s /\.\([0-9]\)/,\1/<br/>
<br/>
Find:     .(dígit 0 to 9)<br/>
Replace:  ,(dígit 0 to 9)<br/>
<br/>
