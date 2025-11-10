
### Descripcion

We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it?Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar).The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.

### Solucion

```

Se busco en los caracteres que nos dio y en la linea 376 estaba la bandera encriptada y utilice ceaser decode para que me diera las bandera.




Flag: picoCTF{C7r1F_54V35_71M3}

```

### Notas



## Referencias

https://www.dcode.fr/caesar-cipher