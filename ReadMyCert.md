# ReadMyCert Problem

__Problem Link:__ [ReadMyCert](https://play.picoctf.org/practice/challenge/367?category=2&page=3)
---

__Description:__ How about we take you on an adventure on exploring certificate signing requests 

Take a look at this CSR file [here](https://artifacts.picoctf.net/c/425/readmycert.csr).

__Hint:__ Download the certificate signing request and try to read it.

## Tools to SOLVE:

- cat - a python command to read file
- [CSR Decoder](https://www.ssldragon.com/ssl-tools/decode-csr/)  

### My Approach:
```
1. Open the file csr formatted file with cat file.
2. Copy the information of the file into the CSR Decoder website
3. After clicking Decode CSR, in the Common Name section the result is shown that is the flag.
4. Then PEEAAACCCCEEEEEEEEEEE!!!!!!!!
```

### flag : ~~picoCTF{read_mycert_693f7c03}~~
_Note:_ Don't copy it try yourself.