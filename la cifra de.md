
### Descripcion

I found this cipher in an old book. Can you figure out what it says? Connect with `nc jupiter.challenges.picoctf.org 58295`.

### Solucion

```

Al recibir el mensaje despues de ejecutar el nc, lo fuimos a descifrar a cybercher con vigenere decode y te dara un texto largo en ingles y la llave para el vigenere decode es "flag"

Este es el texto: For the implementation of this cipher a table is formed by sliding the lower half of an ordinary alphabet for an apparently random number of places with respect to the upper halfpicoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a} The first well-documented description of a polyalphabetic cipher however, was made around 1467 by Leon Battista Alberti.

The Vigenère Cipher is therefore sometimes called the Alberti Disc or Alberti Cipher.

In 1508, Johannes Trithemius invented the so-called tabula recta (a matrix of shifted alphabets) that would later be a critical component of the Vigenère Cipher.

Bellaso’s second booklet appeared in 1555 as a continuation of the first. The lower halves of the alphabets are now shifted regularly, but the alphabets and the index letters are mixed by means of a mnemonic key phrase, which can be different with each correspondent.

flag: picoCTF{b311a50_0r_v1gn3r3_c1ph3ra966878a}

```

### Notas



## Referencias