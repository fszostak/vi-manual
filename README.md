VI - Manual by Fabio Szostak!
===================


VI command summary. Enjoy and increase it. You're welcome.

----------

<table border="2" width="0">
<tr>
<td>

*Basic commands*

**Edition**

:e file ope**n**<br/>
:e! file open with ignore changes<br/>
:e# ou :e!# open previous file<br/>
:wq ou :x ou :x! save and exit<br/>
!!cmd  run command and get output<br/>

**Navigation**

<kbd>h</kbd> like arrow left <br/>
<kbd>j</kbd> like arrow dow**n**<br/>
<kbd>k</kbd> like arrow up<br/>
<kbd>l</kbd> like arrow right<br/>
<kbd>0</kbd> begin of line<br/>
<kbd>$</kbd> end of line<br/>
<kbd>H</kbd> top of scree**n**<br/>
<kbd>L</kbd> bottom of scree**n**<br/>
<kbd>w</kbd> begin next word<br/>
<kbd>e</kbd> end next word<br/>
<kbd>b</kbd> back previous word<br/>
<kbd>CTRL-F</kbd> like PG-DOWN<br/>
<kbd>CTRL-B</kbd> like PG-UP<br/>
<kbd>G</kbd>  go end of file<br/>
:n go to line number ($=end)<br/>

**Search**

<kbd>/</kbd> str find next match<br/>
<kbd>?</kbd> str find previous match<br/>
<kbd>%</kbd>  find close char {}()[]<br/>

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
<kbd>d</kbd> + <kbd>d</kbd>  delete current line<br/>
:g/regexp/d delete all lines match regexp<br/>

**Replace**
<kbd>r</kbd>   replace one character <br/>
<kbd>R</kbd>   enter in replace mode<br/>
<kbd>c</kbd>+<kbd>w</kbd>  replace current word<br/>
<kbd>s</kbd>  replace one char and enter in replace mode<br/>
:x,y s /search/replace/g find and replace<br/> (x,y = line range, % is oll, g is all occurences in line)<br/>
<kbd>~</kbd> change character case (uppercase|lowercase)<br/>

**Join lines**

<kbd>J</kbd>  Join current line with next line<br/>

**Repeat**

<kbd>.</kbd>  Repeat last command<br/>

**Indent**

<kbd>>></kbd> shift current line to right<br/>
<kbd><<</kbd> shift current line to left<br/>

**Copy to buffer**

<kbd>y</kbd> + <kbd>y</kbd> copy current line to temporary buffer<br/>
<kbd>Y</kbd> copy current line to temporary buffer<br/>

**Paste buffer**

<kbd>P</kbd> paster buffer previous<br/>
<kbd>p</kbd> paste buffer next<br/>

**Mark**
<kbd>m</kbd>[a-z] put mark in current line<br/>
<kbd>’</kbd>[a-z] go to mark<br/>
<kbd>’</kbd> + <kbd>’</kbd> go to last mark<br/>

</td>
<td>
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
**n**<kbd>d</kbd> + <kbd>d</kbd> **n** lines<br/>
<kbd>d</kbd>/str até encontrar str<br/>
<kbd>d</kbd>% delete to match character {}[]()<br/>
<kbd>d</kbd>G delete to end of file<br/>
<kbd>d</kbd>1G delete to begining of file<br/>
<kbd>d</kbd>nG delete to begining of file, except **n** first lines<br/>
<kbd>d</kbd>w delete to end of word<br/>
<kbd>d</kbd>nw delete **n** words<br/>

**Replace**

**n**<kbd>s</kbd> **n** characters<br/>
<kbd>c</kbd>**n**<kbd>w</kbd> **n** palavras<br/>
<kbd>c</kbd><kbd>$</kbd> do cursor até o final da
   linha<br/>
<kbd>c</kbd><kbd>0</kbd> do cursor até o início
   da linha<br/>
<kbd>c</kbd><kbd>/</kbd>str até encontrar str<br/>
<kbd>c</kbd><kbd>%</kbd> grupo de linhas/ 
   caracteres {}[]()<br/>
<kbd>c</kbd><kbd>G</kbd> até final do arquivo<br/>



**Join lines**

nJ **n** linhas logo abaixo da corrente<br/>

**Indent**

n>> **n** linhas a direita<br/>
**n**<< **n** linhas a esquerda<br/>
>% bloco a direita<br/>
<% bloco a esquerda<br/>
>G corrente até o final do arquivo<br/>
>1G corrente até o início do arquivo<br/>
>/str corrente até encontrar str<br/>

**Registers**


“[a-z] indicar utilização de registrador <br/>
@[a-z] executa comandos registrador <br/>


**Copy to register**

“ryy reg “r” com a linha corrente<br/>
“ry’m reg “r” com o texto até 
      encontrar a marca “m”<br/>
“ry/str reg “r” com texto até
        encontrar a string “str”<br/>
“ry$ reg “r” com texto até o final da
     linha<br/>
“ryw reg “r” com uma palavra<br/>

**Paste from register**

“rp reg “r” após cursor/linha<br/>
“rP reg “r” antes cursor/linha<br/>

</td>
</tr>
</table>


**RegExp Example**

DICA: Como fazer para trocar de uma só vez todas linhas abaixo de "." por ","<br/>
<br/>
 ARQUIVO ORIGINAL      ARQUIVO ALTERADO<br/>
 ........ 1234.10  =>  ........ 1234,10 <br/>
 ........ 2233.20  =>  ........ 2233,20 <br/>
<br/>
Comando:       :1,$ s /\.\([0-9]\)/,\1/<br/>
<br/>
Pesquisar por:   .(dígito de 0 a 9)<br/>
Substituir por:  ,(dígito de 0 a 9)<br/>
<br/>
Obs.: o "\1" refere-se ao primeiro (), para os demais será necessário referenciar "\2", "\3", "\4", etc.<br/>

