

### Descripcion

Our flag printing service has started glitching!

Additional details will be available after launching your challenge instance.

### Solucion
Te conectas al servidor
```
iTheGuiller-picoctf@webshell:~$ nc saturn.picoctf.net 61499
'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'

iTheGuiller-picoctf@webshell:~$ 
```

Despues tuve que convertir los valores en chr
```
Python 3.10.12 (main, Feb  4 2025, 14:57:36) [GCC 11.4.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> 'picoCTF{gl17ch_m3_n07_' + chr(0x61) + chr(0x34) + chr(0x33) + chr(0x39) + chr(0x32) + chr(0x64) + chr(0x32) + chr(0x65) + '}'
'picoCTF{gl17ch_m3_n07_a4392d2e}'
>>> 
```

### Notas


## Referencias