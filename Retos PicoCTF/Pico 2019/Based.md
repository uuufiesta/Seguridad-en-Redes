
# Based
## Descripcion
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 29956`.
## Pistas

## Solucion
Tenemos que convertir desde la base que nos de el dato a texto para poder responder correctamente y obtener la bandera
``` bash
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ nc jupiter.challenges.picoctf.org 29956
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon
Please give me the  163 165 142 155 141 162 151 156 145 as a word.
Input:
submarine
Please give me the 6c696d65 as a word.
Input:
lime
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_b375bb16}
```
## Bandera
picoCTF{learning_about_converting_values_b375bb16}