

### Descripcion

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 14291`.

### Solucion

Primero tienes que conectarte al servidor y al puerto, despues guardar el archivo y buscar la bandera con grep
```
iTheGuiller-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 14291 > salida.txt

iTheGuiller-picoctf@webshell:~$ grep -o "picoCTF{.*}" salida.txt
picoCTF{digital_plumb3r_ea8bfec7}
iTheGuiller-picoctf@webshell:~$ 
```

### Notas

Se puede guardar el texto que te arroja el puerto con ">"
Con grep puedes buscar cierta palabra en el archivo

## Referencias
