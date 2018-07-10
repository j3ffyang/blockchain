## Generate BTC Key

- General key architecture
<img src="../imgs/bitcoin_keys.png">

- Create an Elliptic Curve key-pair based on ```secp256k1``` curves.

```shell
[jeff@f28 ~]$ openssl ecparam -name secp256k1 -genkey -out /tmp/ec-keypair.pem

[jeff@f28 tmp]$ cat ec-keypair.pem
-----BEGIN EC PARAMETERS-----
BgUrgQQACg==
-----END EC PARAMETERS-----
-----BEGIN EC PRIVATE KEY-----
MHQCAQEEINdrFJ7w9LoGEZ0iQR61Ib0Yau5ELE1nuoXrvKdqEgzHoAcGBSuBBAAK
oUQDQgAEtdlfyywoyCpQVkFNQHGDlq8bn0CpOs6ebvb+TZyM8YiCh34mJq6OwbJw
2LKx8PNed+Kf0f6VScdrcQWaRGVSnQ==
-----END EC PRIVATE KEY-----
```

- View the private and public key

```shell
[jeff@f28 tmp]$ openssl ec -in /tmp/ec-keypair.pem -text -noout
read EC key
Private-Key: (256 bit)
priv:
    d7:6b:14:9e:f0:f4:ba:06:11:9d:22:41:1e:b5:21:
    bd:18:6a:ee:44:2c:4d:67:ba:85:eb:bc:a7:6a:12:
    0c:c7
pub:
    04:b5:d9:5f:cb:2c:28:c8:2a:50:56:41:4d:40:71:
    83:96:af:1b:9f:40:a9:3a:ce:9e:6e:f6:fe:4d:9c:
    8c:f1:88:82:87:7e:26:26:ae:8e:c1:b2:70:d8:b2:
    b1:f0:f3:5e:77:e2:9f:d1:fe:95:49:c7:6b:71:05:
    9a:44:65:52:9d
ASN1 OID: secp256k1
```

- Hash the public key using ```SHA256``` followed by ```RIPEMD-160```

[jeff@f28 tmp]$ openssl ec -in /tmp/ec-keypair.pem -pubout -outform DER | tail -c 65 | sha256sum | xxd -r -p | openssl rmd160
read EC key
writing EC key
(stdin)= 327d2921de28063206940d79c7aa2b4896e79737


- Compute the Checksum

[jeff@f28 tmp]$ echo -n "**00**327d2921de28063206940d79c7aa2b4896e79737" | xxd -r -p | sha256sum | xxd -r -p | sha256sum
**7b8ddc4c**165ed9240788545e569f74aea710197956ac4a2e8b33ef3778304397  -

[jeff@f28 tmp]$ b58encode 00327d2921de28063206940d79c7aa2b4896e79737**7b8ddc4c**
```shell
33GNRFw1NiwXy3HXTDemx8UCUqanxJgUK
```

Then the address is **1**33GNRFw1NiwXy3HXTDemx8UCUqanxJgUK

- Reference from Google Images

<img src="../imgs/20170526_generatebitcoinaddr.png" width="650px">
