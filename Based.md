
### Descripcion

To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29221`.

### Solucion

En este reto te pide hacer varias conversiones, primero de binario a texto, despues de octal a texto y por ultimo de hexadecimal a texto. 
Por lo que forma mas facil que me parece para resolverlo es haciendo las conversiones en paginas de conversion, los links a las paginas estan la referencias, abajo.

```
iTheGuiller-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 29221
Let us see how data is stored
animation
Please give the 01100001 01101110 01101001 01101101 01100001 01110100 01101001 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
animation
Please give me the  143 157 155 160 165 164 145 162 as a word.
Input:
computer
Please give me the 636f6e7461696e6572 as a word.
Input:
container
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_00a975ff}

```

### Notas


## Referencias
[http://www.unit-conversion.info/texttools/octal/](http://www.unit-conversion.info/texttools/octal/) [https://www.rapidtables.com/convert/number/hex-to-ascii.html](https://www.rapidtables.com/convert/number/hex-to-ascii.html)