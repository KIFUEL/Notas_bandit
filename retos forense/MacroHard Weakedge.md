## Descripción 
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/3944a59474f9f676942282c50b9c3675/Forensics%20is%20fun.pptm)

## Hits


## Solución
```
Podemos observar que es un archivo PowerPoint de 2007 que solian estar compimidos, entonces lo descomprimimos.
th0rtilla-picoctf@webshell:~/Macro$ unzip Forensics\ is\ fun.pptm 
Archive:  Forensics is fun.pptm
  inflating: [Content_Types].xml     
  inflating: _rels/.rels             
  inflating: ppt/presentation.xml    
  inflating: ppt/slides/_rels/slide46.xml.rels  
  inflating: ppt/slides/slide1.xml   
  ...
  inflating: docProps/core.xml       
  inflating: docProps/app.xml        
  inflating: ppt/slideMasters/hidden 

Fueron muchos archivos, ahora debemos de encontar la bandera entre todos ellos.


th0rtilla-picoctf@webshell:~/Macro$ ls -la *
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 100093 Mar 24  2021 'Forensics is fun.pptm'
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf  10660 Jan  1  1980 '[Content_Types].xml'

_rels:
total 4
drwxrwxr-x 2 th0rtilla-picoctf th0rtilla-picoctf  19 Mar 30 05:33 .
drwxrwxr-x 5 th0rtilla-picoctf th0rtilla-picoctf 102 Mar 30 05:33 ..
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 738 Jan  1  1980 .rels

docProps:
total 12
drwxrwxr-x 2 th0rtilla-picoctf th0rtilla-picoctf   59 Mar 30 05:33 .
drwxrwxr-x 5 th0rtilla-picoctf th0rtilla-picoctf  102 Mar 30 05:33 ..
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 3784 Jan  1  1980 app.xml
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf  666 Jan  1  1980 core.xml
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 2278 Jan  1  1980 thumbnail.jpeg

ppt:
total 40
drwxrwxr-x 7 th0rtilla-picoctf th0rtilla-picoctf 4096 Mar 30 05:33 .
drwxrwxr-x 5 th0rtilla-picoctf th0rtilla-picoctf  102 Mar 30 05:33 ..
drwxrwxr-x 2 th0rtilla-picoctf th0rtilla-picoctf   35 Mar 30 05:33 _rels
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf  818 Jan  1  1980 presProps.xml
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 5197 Jan  1  1980 presentation.xml
drwxrwxr-x 3 th0rtilla-picoctf th0rtilla-picoctf 4096 Mar 30 05:33 slideLayouts
drwxrwxr-x 3 th0rtilla-picoctf th0rtilla-picoctf   57 Mar 30 05:33 slideMasters
drwxrwxr-x 3 th0rtilla-picoctf th0rtilla-picoctf 4096 Mar 30 05:33 slides
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf  182 Jan  1  1980 tableStyles.xml
drwxrwxr-x 2 th0rtilla-picoctf th0rtilla-picoctf   24 Mar 30 05:33 theme
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf 7168 Jan  1  1980 vbaProject.bin
-rw-rw-r-- 1 th0rtilla-picoctf th0rtilla-picoctf  811 Jan  1  1980 viewProps.xml
th0rtilla-picoctf@webshell:~/Macro$ 

El vbaProject.bin podria tener la bandera, asi que buscamos ahí.
th0rtilla-picoctf@webshell:~/Macro$ strings ppt/vbaProject.bin 
VBAProje
stdole>
*\G{00
020430-
6}#2.0#0
#C:\Wind
ows\Syst em32\
tlb#OLE 
Automati
EOffDic
2DF8D04C
-5BFA-10
1B-BDE5
gram Fil
es\Commo
Micros
oft Shar
ed\OFFIC
E16\MSO.0DLL#
M 1@6.0 Ob
Library
ule1G
sorry_but_this_isn't_it
Attribut
e VB_Nam
e = "Mod
ule1"
ub not_f
lag()
L As
@sorry_
this_isn 't_it
CsXz
PowerPoint
Win16
Win32
Win64x
VBA6
VBA7
Project1
stdole
VBAProject
Office
Module1b
_Evaluate
not_flag
ID="{111D4352-E1AC-46B0-8500-E5E7DFB7004C}"
Module=Module1
Name="VBAProject"
HelpContextID="0"
VersionCompatible32="393222000"
CMG="3436F0FDF000F400F400F400F4"
DPB="3B39FFFA07FB07FB07"
GC="424086038C048C0473"
[Host Extender Info]
&H00000001={3832D640-CF90-11CF-8E43-00A0C911005A};VBE;&H00000000
[Workspace]
Module1=26, 26, 668, 718, 
Module1

No encontramos nada, nos vamos a ppt/slideMasters/hidden
th0rtilla-picoctf@webshell:~/Macro$ cat ppt/slideMasters/hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q
th0rtilla-picoctf@webshell:~/Macro$ 

Lo mas probable es que sea base 64, quitamos los espacios y vamos a una paguina a traducirlo a ASCII

ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ

flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}
```

## Bandera
picoCTF{D1d_u_kn0w_ppts_r_z1p5}