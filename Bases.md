
### Descripcion
What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.


### Solucion
### Forma 1
cybercheck
from base 64

PicoCTF(l3arn_th3_r0p35)

### Forma 2

```
import base64

encoded = "bDNhcm5fdGgzX3IwcDM1"
decoded = base64.b64decode(encoded).decode("utf-8")

print(decoded)  # l3arn_th3_r0p35

```

### Notas


### Referencias
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkROaGNtNWZkR2d6WDNJd2NETTE