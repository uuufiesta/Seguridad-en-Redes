
# First Grep
## Descripcion
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/515f19f3612bfd97cd3f0c0ba32bd864/file)? This would be really tedious to look through manually, something tells me there is a better way.
## Pistas

## Solucion
``` bash
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ ls
file  strings
                                                                                
┌──(pariboy㉿uuufiesta)-[~/Descargas]
└─$ cat file| grep pico'        
picoCTF{grep_is_good_to_find_things_5af9d829}
```
## Bandera
picoCTF{grep_is_good_to_find_things_5af9d829}