Name | Type | Points 
---|---|---
Mod 26 | Cryptography | 10

AUTHOR: PANDU  
Description: Cryptography can be easy, do you know what ROT13 is?  
cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}  

Resolution:
Rot13 is a simple substitution cipher where you substitute the alphanumerical value with the value of +13.

The tr command in shell is translate, we can use it to import a string and substitute manually.

```shell
tysonz-picoctf@webshell:~$ echo "cvpbPGS{arkg_gvzr_V'yy_gel_2_ebhaqf_bs_ebg13_Ncualgvd}" | tr '[A-Za-z]' '[N-ZA-Mn-za-m]'
picoCTF{next_time_I'll_try_2_rounds_of_rot13_Aphnytiq}
```