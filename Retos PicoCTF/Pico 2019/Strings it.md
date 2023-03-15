
# Strings it
## Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Pistas

## Solucion
``` bash
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ cd /home/pariboy/Descargas/            
                                                                                
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ ls                         
strings
                                                                                
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ strings strings| grep pico' 
picoCTF{5tRIng5_1T_7f766a23}

```
## Bandera
picoCTF{5tRIng5_1T_7f766a23}