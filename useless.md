
### Descripcion

There's an interesting script in the user's home directory

Additional details will be available after launching your challenge instance.

### Solucion


```
iTheGuiller-picoctf@webshell:~$ ssh -p 59504 picoplayer@saturn.picoctf.net
picoplayer@saturn.picoctf.net's password: 
Welcome to Ubuntu 20.04.6 LTS (GNU/Linux 6.8.0-1035-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage

The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

picoplayer@challenge:~$ ls
useless
picoplayer@challenge:~$ cat useless
#!/bin/bash
# Basic mathematical operations via command-line arguments

if [ $# != 3 ]
then
  echo "Read the code first"
else
        if [[ "$1" == "add" ]]
        then 
          sum=$(( $2 + $3 ))
          echo "The Sum is: $sum"  

        elif [[ "$1" == "sub" ]]
        then 
          sub=$(( $2 - $3 ))
          echo "The Substract is: $sub" 

        elif [[ "$1" == "div" ]]
        then 
          div=$(( $2 / $3 ))
          echo "The quotient is: $div" 

        elif [[ "$1" == "mul" ]]
        then
          mul=$(( $2 * $3 ))
          echo "The product is: $mul" 

        else
          echo "Read the manual"
         
        fi
fi
picoplayer@challenge:~$ man useless

useless
     useless, -- This is a simple calculator script

SYNOPSIS
     useless, [add sub mul div] number1 number2

DESCRIPTION
     Use the useless, macro to make simple calulations like addition,subtraction, multiplication and division.

Examples
     ./useless add 1 2
       This will add 1 and 2 and return 3

     ./useless mul 2 3
       This will return 6 as a product of 2 and 3

     ./useless div 6 3
       This will return 2 as a quotient of 6 and 3

     ./useless sub 6 5
       This will return 1 as a remainder of substraction of 5 from 6

Authors
     This script was designed and developed by Cylab Africa

     picoCTF{us3l3ss_ch4ll3ng3_3xpl0it3d_6140}

picoplayer@challenge:~$ 
```

### Notas

El comando **`man useless`** en sistemas Unix/Linux intenta mostrar la página del manual para el comando `useless`. Sin embargo, si `useless` no es un comando válido o no está instalado, recibirás un mensaje indicando que no hay página de manual disponible para él.

### Qué sucede cuando ejecutas `man useless`:

[](https://github.com/armandoportillo0101/Seguridad-de-Redes/blob/main/Problemas_parcial1_pico/useless.md#qu%C3%A9-sucede-cuando-ejecutas-man-useless)

- **Si el comando no existe**: Verás un mensaje como "No manual entry for useless" o "No manual entry for `useless`" si `useless` no está instalado o no tiene una página de manual.
    
- **Si el comando existe**: Verás la página del manual correspondiente al comando `useless`, si es que existe y está instalado.

## Referencias