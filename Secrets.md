
### Descripcion

We have several pages hidden. Can you find the one with the flag?

Additional details will be available after launching your challenge instance.

### Solucion

```

Accedemos a la herramienta “Inspeccionar” haciendo clic derecho. Si vamos a las fuentes, podemos ver los archivos que se encuentran dentro del directorio assets. Observamos que el directorio assets se encuentra dentro de un directorio “secreto”.
Acceder a un directorio a través de URL:
Si escribe picoctf.net/secret/ en su navegador: Si el listado de directorios está activado y no hay un archivo de índice (como index.html), el servidor le mostrará una lista de archivos en la carpeta secreta. Si el listado de directorios está desactivado pero hay un archivo de índice, el servidor mostrará ese archivo y verá una página web.
Visitemos el directorio secreto y veamos qué nos devuelve el servidor web. Vayamos a “…/secret/”.
Continuar hasta “…/secret/hidden/” conduce a una página con otro directorio llamado “superhidden”.
Finalmente, al acceder a la página “superhidden” se revela la bandera

Flag: picoCTF{succ3ss_@h3n1c@10n_790d2615}

```

### Notas



## Referencias