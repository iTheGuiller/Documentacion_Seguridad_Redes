
### Descripcion
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

### Solucion
Se utilizo el "chr" para convertir (código Unicode o ASCII) en el **carácter** que representa.

```
iTheGuiller-picoctf@webshell:~$ python
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x70))
p
```

### Notas


## Referencias

https://webshell.picoctf.org