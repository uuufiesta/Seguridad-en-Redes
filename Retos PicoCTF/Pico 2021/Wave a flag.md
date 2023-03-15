
# Wave a flag
## Descripcion
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Pistas

## Solucion
``` bash
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ strings warm | grep pico       
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
```
## Bandera
picoCTF{b1scu1ts_4nd_gr4vy_616f7182}