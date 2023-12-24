# Mind your Ps and Qs Problem

__Problem Link:__ [Mind your Ps and Qs](https://play.picoctf.org/practice/challenge/162?category=2&page=1)
---

__Description:__ In RSA, a small e value can be problematic, but what about N? Can you decrypt this? [values](https://mercury.picoctf.net/static/bf5e2c8811afb4669f4a6850e097e8aa/values)

## Tools to SOLVE: 

- [factordb](https://factordb.com/)

<br>

__Hint:__ Bits are expensive, I used only a little bit over 100 to save money

### My Approach:
```
1. First read about RSA in WIKIPEDIA
2. Understand the basic trick to solve the RSA
3. Three fundamental numbers for RSA are n{prime multiplication of p and q}, d{decryption key}, c{cipher text}.
4. Write the code in any coding language.
5. Give the the present value.
6. Use factordb.com to calculate the prime factor
7. After few operation the flag is visible.
```
<br>

```python
from Crypto.Util.number import *

c = 421345306292040663864066688931456845278496274597031632020995583473619804626233684
n = 631371953793368771804570727896887140714495090919073481680274581226742748040342637
e = 65537

p = 1461849912200000206276283741896701133693    #factor of N
q = 431899300006243611356963607089521499045809  #factor of N

phi = (p-1) * (q-1)

d = inverse( e, phi)

m = pow(c, d, n)        # c^d mod n

print(long_to_bytes(m))

```
### flag : ~~picoCTF{sma11_N_n0_g0od_00264570}~~ 
<br>

_Note:_ Don't copy it try yourself.