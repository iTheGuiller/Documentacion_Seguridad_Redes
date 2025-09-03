

### Descripcion

Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/static)? This [BASH script](https://mercury.picoctf.net/static/ff4e569d6b49b92d090796d4631a2577/ltdis.sh) might help!

### Solucion

```
iTheGuiller-picoctf@webshell:~$ ls
README.txt  file  file2  flag  ltdis.sh  salida.txt  static  strings  warm
iTheGuiller-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_ccb2b43e}
iTheGuiller-picoctf@webshell:~$ 
```

### Notas

El comando `strings static | grep pico` funciona de manera muy similar al ejemplo anterior, pero en este caso, se está analizando un archivo llamado `static`.

- **`strings static`**: Extrae todas las secuencias de texto legible del archivo llamado `static`. Esto es útil cuando `static` es un archivo binario o cualquier archivo que no sea fácilmente legible de forma directa.
- **`| grep pico`**: Luego filtra la salida de `strings` para mostrar solo las líneas que contienen la palabra "pico".[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Plantilla.md#notas-adicionales)

## Referencias