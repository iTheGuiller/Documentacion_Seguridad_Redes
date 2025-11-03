
### Descripcion

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)


### Solucion

```
al ejecutar el ultimo comando mostrado nos mostrara una pantalla en la que tendremos que combinar las dos imágenes que descargamos al principio. Abres la primera imagen, después abres el menú de analyse y seleccionas la opcion de combiner y eliges la segunda imagen. Después de hacer todo lo anterior te dará la bandera.


sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar

sudo chmod +x stegsolve.jar

mkdir bin

mv stegsolve.jar bin/

java -jar stegsolve.jar


flag: picoCTF{2a4d45c7}

```

### Notas



## Referencias