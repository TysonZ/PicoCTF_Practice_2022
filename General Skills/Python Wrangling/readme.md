Name | Type | Points 
---|---|---
Python Wrangling | General Skills | 10

AUTHOR: SYREAL
Description

Python scripts are invoked kind of like programs in the Terminal... Can you run this Python script(https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py) using this password(https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt) to get the flag(https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en)?

# Resolution:
### Download Files
```shell 
wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/ende.py
wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/pw.txt
wget https://mercury.picoctf.net/static/b351a89e0bc6745b00716849105f87c6/flag.txt.en
python3 ende.py 
cat pw.txt | python3 ende.py -d flag.txt.en       
Please enter the password:picoCTF{4p0110_1n_7h3_h0us3_67c6cc96}
```
### 