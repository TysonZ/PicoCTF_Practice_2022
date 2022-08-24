Name | Type | Points 
---|---|---
Information | Forensics | 10

AUTHOR: SUSIE  
Description: Files can always be changed in a secret way. Can you find the flag? cat.jpg(https://mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg)  

# Resolution
```Shell
wget https://mercury.picoctf.net/static/a614a27d4cb251d04c7d2f3f3f76a965/cat.jpg
vi cat.jpg
```
### Read the image data
```
^@^PJFIF^@^A^B^@^@^A^@^A^@^@^@0Photoshop 3.0^@8BIM^D^D^@^@^@^@^@^S^\^Bt^@^GPicoCTF^\^B^@^@^B^@^D^@^Khttp://ns.adobe.com/xap//
1.0/^@<?xpacket begin='' id='W5M0MpCehiHzreSzNTczkc9d'?>
<x:xmpmeta xmlns:x='adobe:ns:meta/' x:xmptk='Image::ExifTool 10.80'>
<rdf:RDF xmlns:rdf='http://www.w3.org/1999/02/22-rdf-syntax-ns#'>

 <rdf:Description rdf:about=''
  xmlns:cc='http://creativecommons.org/ns#'>
  <cc:license rdf:resource='cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9'/>
 </rdf:Description>

 <rdf:Description rdf:about=''
  xmlns:dc='http://purl.org/dc/elements/1.1/'>
  <dc:rights>
   <rdf:Alt>
    <rdf:li xml:lang='x-default'>PicoCTF</rdf:li>
   </rdf:Alt>
  </dc:rights>
 </rdf:Description>
</rdf:RDF>
</x:xmpmeta>
```

### Stuck
*Here I attempted to submit the ID and License values as the picoCTF{flag}, this did not work.*
#### Base64 Decode
```
echo 'W5M0MpCehiHzreSzNTczkc9d' | base64 --decode
echo 'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9' | base64 --decode
picoCTF{the_m3tadata_1s_modified}
```