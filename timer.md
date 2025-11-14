
### Descripcion

You will find the flag after analysing this apkDownload [here](https://artifacts.picoctf.net/c/449/timer.apk).

### Solucion

```

Solo se tuvo que extraer el archivo y se busco un documento en especifico:

find . -name classes3.dex

y despues solo se hace un cat para buscar la flag

strings classes3.dex | grep pico

Flag: picoCTF{t1m3r_r3v3rs3d_succ355fully_17496}

```

### Notas



## Referencias