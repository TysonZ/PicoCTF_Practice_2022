Name | Type | Points 
---|---|---
Wave a Flag | General Skills | 10

AUTHOR: SYREAL  
Description: Can you invoke help flags for a tool or binary? This program(https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm) has extraordinarily helpful information...  

# Resolution
```Shell
wget https://mercury.picoctf.net/static/cfea736820f329083dab9558c3932ada/warm
chmod +x warm
./warm
./warm -h
picoCTF{b1scu1ts_4nd_gr4vy_30e77291}
```