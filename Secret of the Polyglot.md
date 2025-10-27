
### Descripcion

The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/98/flag2of2-final.pdf).

### Solucion

```

Desde exiftool, sabemos que hay algo oculto después del fragmento IEND, podemos desplazarnos hasta la parte inferior o usar la búsqueda y el filtro. Desde aquí, veremos una firma de encabezado PDF después del fragmento final del PNG. Podemos extraer el hexadecimal PDF en un nuevo archivo y guardarlo como flag.pdf, pero recuerda empezar desde `25 50 44 46`. Copie y pegue el PDF hexadecimal en un nuevo archivo y lo guarde como output.pdf.

Por ultimo solo lo abri y me dio la segunda parte de la bandera, ya que en este reto se nos da la bandera en dos partes.

Flag. picoCTF{f1u3n7_1n_pn9_&_pdf_1f991f77}


```

### Notas



## Referencias