VI - Manual by Fabio Szostak!
===================


VI command summary. Enjoy and increase it. You're welcome.

----------
**Edição**

Press <kbd>Esc</kbd> and type
```
:e /path/of/filename
```
**Open a file ignoring the current changes**

Press <kbd>Esc</kbd> and type
```
:e! /path/of/filename
```

*Basic commands*

**Edition**

:e file open
:e! file open with ignore changes
:e# ou :e!# open previous file
:wq ou :x ou :x! save and exit
!!cmd  run command and get output

**Movimentação**

<kbd>h</kbd> like arrow left 
<kbd>j</kbd> like arrow down
<kbd>k</kbd> like arrow up
<kbd>l</kbd> like arrow right
<kbd>0</kbd> begin of line
<kbd>$</kbd> end of line
<kbd>H</kbd> top of screen
<kbd>L</kbd> bottom of screen
<kbd>w</kbd> begin next word
<kbd>e</kbd> end next word
<kbd>b</kbd> back previous word
<kbd>CTRL-F</kbd> like PG-DOWN
<kbd>CTRL-B</kbd> like PG-UP
<kbd>G</kbd>  go end of file
:n go to line number ($=end)

**Search**

<kbd>/</kbd> str find next match
<kbd>?</kbd> str find previous match
<kbd>%</kbd>  find close char {}()[]

**Insert**
 
<kbd>i</kbd>  enter in insert mode
<kbd>I</kbd>  enter insert mode at begin of line
<kbd>a</kbd>  at next character
<kbd>A</kbd>  enter insert mode at end of file
<kbd>o</kbd>  enter insert mode at next line
<kbd>O</kbd>  enter insert mode at previous line


**Undo changes**
<kbd>u</kbd>  last command
<kbd>U</kbd>  all commands in current line


**Delete**
<kbd>x</kbd>  delete current character
<kbd>d</kbd> + <kbd>d</kbd>  delete current line
:g/regexp/d delete all lines match regexp

**Replace**
<kbd>r</kbd>   replace one character 
<kbd>R</kbd>   enter in replace mode
<kbd>c</kbd>+<kbd>w</kbd>  replace current word
<kbd>s</kbd>  replace one char and enter in replace mode
:x,y s /search/replace/g find and replace (x,y = line range, % is oll, g is all occurences in line)
<kbd>~</kbd> change character case (uppercase|lowercase)

**Join lines**

<kbd>J</kbd>  Join current line with next line

**Repeat**

<kbd>.</kbd>  Repeat last command

**Indent**

<kbd>>></kbd> shift current line to right
<kbd><<</kbd> shift current line to left

**Copy to buffer**

<kbd>y</kbd> + <kbd>y</kbd> copy current line to temporary buffer
<kbd>Y</kbd> copy current line to temporary buffer

**Paste buffer **

<kbd>P</kbd> paster buffer previous
<kbd>p</kbd> paste buffer next

**Mark**
<kbd>m</kbd>[a-z] put mark in current line
<kbd>’</kbd>[a-z] go to mark
<kbd>’</kbd> + <kbd>’</kbd> go to last mark

*Advanced commands*

**Movimentação**

<kbd>nh n caracteres a esquerda 
nj n linhas a baixo
nk n linhas a cima
nl n caracteres a direita

nw n palavras
ne n palavras
nb volta n palavras

nG n linhas do início 
   arquivo

**Inserir**

ni inserir n vezes
nI inserir n vezes
na inserir n vezes
nA inserir n vezes

**Apagar**

nx n caracteres
ndd n linhas
d/str até encontrar str
d% bloco de linhas/ 
   caracteres {}[]()
dG até final do arquivo
d1G até início do arquivo
dnG até n linhas do início
    do arquivo
dw palavra
dnw n palavras

**Substituir**

ns n caracteres
cnw n palavras
c$ do cursor até o final da
   linha
c0 do cursor até o início
   da linha
c/str até encontrar str
c% grupo de linhas/ 
   caracteres {}[]()
cG até final do arquivo



**Juntar linhas**

nJ n linhas logo abaixo da corrente

**Indentar**

n>> n linhas a direita
n<< n linhas a esquerda
>% bloco a direita
<% bloco a esquerda
>G corrente até o final do arquivo
>1G corrente até o início do arquivo
>/str corrente até encontrar str

**Registradores (reg)**


“[a-z] indicar utilização de registrador 
@[a-z] executa comandos registrador 


**Armazenar em registradores**

“ryy reg “r” com a linha corrente
“ry’m reg “r” com o texto até 
      encontrar a marca “m”
“ry/str reg “r” com texto até
        encontrar a string “str”
“ry$ reg “r” com texto até o final da
     linha
“ryw reg “r” com uma palavra

**Liberar conteúdo de registradores**

“rp reg “r” após cursor/linha
“rP reg “r” antes cursor/linha


**RegExp Example**

DICA: Como fazer para trocar de uma só vez todas linhas abaixo de "." por ","

 ARQUIVO ORIGINAL      ARQUIVO ALTERADO
 ........ 1234.10  =>  ........ 1234,10 
 ........ 2233.20  =>  ........ 2233,20 

Comando:       :1,$ s /\.\([0-9]\)/,\1/

Pesquisar por:   .(dígito de 0 a 9)
Substituir por:  ,(dígito de 0 a 9)

Obs.: o "\1" refere-se ao primeiro (), para os demais será necessário referenciar "\2", "\3", "\4", etc.

