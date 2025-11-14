
### Descripcion

What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/289/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?

### Solucion

```

Solo se utilizo este comando para poder encontrar la bandera:

strings -t x SafeOpener.class | grep picoCTF

Flag: picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_de45efd6}

```

### Notas



## Referencias