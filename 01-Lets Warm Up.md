


**Descripcion
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

**Solucion
'picoCTF(p)'

```
pypiTheGuiller-picoctf@webshell:~$ phyton
-bash: phyton: command not found
iTheGuiller-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int (0x70)
112
>>> chr(112)
'p'
>>> 
```


**Notas
Siempre hay que poner la solucion en formato de la bandera

**Referencias
https://gchq.github.io/CyberChef/
