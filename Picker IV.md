
### Descripcion

Can you figure out how this program works to get the flag?

Additional details will be available after launching your challenge instance.

### Solucion

```

Se tuvo que hacer un grep en el archivo que se nos da para encontrar la entrada que debemos poner para que nos de la bandera correcta:

readelf -a picker-IV | grep win

guillermo@MacBook-Pro-de-Guillermo PICO % nc saturn.picoctf.net 56300

Enter the address in hex to jump to, excluding '0x': 0x40129e

You input 0x40129e

You won!

picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}

guillermo@MacBook-Pro-de-Guillermo PICO %

Flag: picoCTF{n3v3r_jump_t0_u53r_5uppl13d_4ddr35535_14bc5444}


```

### Notas



## Referencias