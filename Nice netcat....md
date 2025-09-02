

### Descripcion

There is a nice program that you can talk to by using this command in a shell: `$ nc mercury.picoctf.net 21135`, but it doesn't speak English...
### Solucion

Primero me conecte al servidor
```
iTheGuiller-picoctf@webshell:~$ nc mercury.picoctf.net 21135
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
97 
102 
100 
53 
102 
100 
97 
52 
125 
10 
```

se convirtió en cyberchef y el resultado fue
picoCTF{g00d_k1tty!_n1c3_k1tty!_afd5fda4}

### Notas
Se utilizo cyberchef, from decimal

## Referencias
https://gchq.github.io/CyberChef/#recipe=From_Decimal('Space',false)&input=MTEyIAoxMDUgCjk5IAoxMTEgCjY3IAo4NCAKNzAgCjEyMyAKMTAzIAo0OCAKNDggCjEwMCAKOTUgCjEwNyAKNDkgCjExNiAKMTE2IAoxMjEgCjMzIAo5NSAKMTEwIAo0OSAKOTkgCjUxIAo5NSAKMTA3IAo0OSAKMTE2IAoxMTYgCjEyMSAKMzMgCjk1IAo5NyAKMTAyIAoxMDAgCjUzIAoxMDIgCjEwMCAKOTcgCjUyIAoxMjUgCjEwIA