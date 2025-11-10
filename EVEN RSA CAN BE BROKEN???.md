
### Descripcion

This service provides you an encrypted flag. Can you decrypt it with just N & e?Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 51466`The program's source code can be downloaded [here](https://challenge-files.picoctf.net/c_verbal_sleep/c798cbe85b3e431345406f393827b9b905481b5fcd6d4b4a845527ee0602da9b/encrypt.py).

### Solucion

```

Se realizo un script para poder resolver el reto el cual fue:

from Crypto.Util.number import long_to_bytes

# --- TUS VALORES DEL RETO ---
N = 14966250627256988437764765132310993171225300045392913371379477643862239992781731787593103451647386180467018332425663642360718516859941629269440955072609622
e = 65537
c = 64468311285251305178313480921511985070470524593254409440954997229675198008504707430134618608578246946099427497592836351231565914541275875278049834025595
# ----------------------------------

print("Iniciando ataque...\n")

# 1. Explotar la vulnerabilidad (N es par)
# Si N es par, uno de sus factores primos (p) debe ser 2.
p = 2

# 2. Encontrar el otro factor primo (q)
# Sabemos que N = p * q, por lo tanto q = N / p
q = N // p

print(f"[+] p encontrado: {p}")
print(f"[+] q encontrado: {q}\n")

# 3. Calcular phi_N (Totient de Euler)
# phi_N = (p - 1) * (q - 1)
# Como p = 2, esto se simplifica a: (2 - 1) * (q - 1) = 1 * (q - 1)
phi_N = q - 1

print(f"[+] phi_N calculado: {phi_N}\n")

# 4. Calcular la clave privada (d)
# 'd' es el inverso modular de 'e' módulo phi_N
# d = e^(-1) mod phi_N
d = pow(e, -1, phi_N)

print(f"[+] Clave privada (d) calculada.\n")

# 5. Descifrar el mensaje (m)
# m = c^d mod N
m = pow(c, d, N)

print(f"[+] Mensaje descifrado (como número): {m}\n")

# 6. Convertir el número del mensaje a texto
flag = long_to_bytes(m)

# Imprimir la flag
print(f"==============================")
print(f"FLAG: {flag.decode('utf-8')}")
print(f"==============================")

los valores nos los dan entrando al servidor que nos dan para conectarnos.


picoCTF{tw0_1$_pr!m341c6ed35}

```

### Notas



## Referencias