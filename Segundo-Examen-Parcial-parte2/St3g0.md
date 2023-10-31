# St3g0
# Objetivo
Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/215/pico.flag.png)
# Solución 
```
┌──(kali㉿kali)-[~/Documents/retos-examen/Lokey-here/St3g0]
└─$ ls
pico.flag.png
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/retos-examen/Lokey-here/St3g0]
└─$ sudo apt install ruby                   
[sudo] password for kali: 
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
ruby is already the newest version (1:3.1).
ruby set to manually installed.
0 upgraded, 0 newly installed, 0 to remove and 0 not upgraded.
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/retos-examen/Lokey-here/St3g0]
└─$ sudo gem install zsteg
Fetching rainbow-3.1.1.gem
Fetching iostruct-0.0.5.gem
Fetching zsteg-0.2.13.gem
Fetching zpng-0.4.5.gem
Successfully installed rainbow-3.1.1
Successfully installed zpng-0.4.5
Successfully installed iostruct-0.0.5
Successfully installed zsteg-0.2.13
Parsing documentation for rainbow-3.1.1
Installing ri documentation for rainbow-3.1.1
Parsing documentation for zpng-0.4.5
Installing ri documentation for zpng-0.4.5
Parsing documentation for iostruct-0.0.5
Installing ri documentation for iostruct-0.0.5
Parsing documentation for zsteg-0.2.13
Installing ri documentation for zsteg-0.2.13
Done installing documentation for rainbow, zpng, iostruct, zsteg after 1 seconds
4 gems installed
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/retos-examen/Lokey-here/St3g0]
└─$ zteg pico.flag.png 
Command 'zteg' not found, did you mean:
  command 'ztee' from deb zmap
Try: sudo apt install <deb name>
                                                                                                                    
┌──(kali㉿kali)-[~/Documents/retos-examen/Lokey-here/St3g0]
└─$ zsteg pico.flag.png 
b1,r,lsb,xy         .. text: "~__B>wV_G@"
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}$t3g0"
b1,abgr,lsb,xy      .. text: "E2A5q4E%uSA"
b2,b,lsb,xy         .. text: "AAPAAQTAAA"
b2,b,msb,xy         .. text: "HWUUUUUU"
b3,r,lsb,xy         .. file: gfxboot compiled html help file
b4,r,lsb,xy         .. file: Targa image data (16-273) 65536 x 4097 x 1 +4352 +4369 - 1-bit alpha - right "\021\020\001\001\021\021\001\001\021\021\001"
b4,g,lsb,xy         .. file: 0420 Alliant virtual executable not stripped
b4,b,lsb,xy         .. file: Targa image data - Map 272 x 17 x 16 +257 +272 - 1-bit alpha "\020\001\021\001\021\020\020\001\020\001\020\001"                                                                                            
b4,bgr,lsb,xy       .. file: Targa image data - Map 273 x 272 x 16 +1 +4113 - 1-bit alpha "\020\001\001\001"
b4,rgba,msb,xy      .. file: Applesoft BASIC program data, first line number 8

```
instale dos herramientas que me ayudaron para encontrar la llave la cual se encuentra en el resultado del ultimo comando

picoCTF{7h3r3_15_n0_5p00n_96ae0ac1}
# Notas Adicionales

# Referencias
https://wiki.bi0s.in/steganography/zsteg/