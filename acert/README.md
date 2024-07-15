# Description

Simple test of ACERT support (Attribute Certificates, RFC 5755) with wolfSSL.

## Prerequisites

Build wolfSSL with attribute certificate support enabled:

```sh
$ ./configure --enable-acert  --enable-opensslextra
$ make
$ sudo make install
```

## Building the example

## Running the example

```sh
./test_acert -f ../certs/acerts/acert.pem
test_acert -f certs/acert.pem
info: using acert: certs/acert.pem
Attribute Certificate:
    Data:
        Version: 2 (0x1)
        Serial Number: 1 (0x1)
        Holder:
            Issuer: CN=TPM Manufacturer
            Serial Number:
                40:0c:7a:06:2d:83:bb:8b:d1:9f:57:66:33:da:ba:e5:44:50:cf:4a
        Issuer: C=US, O=example.com, OU=PCTest
        Validity
            Not Before: Jan  1 05:00:00 2018 GMT
            Not After : Jan  1 05:00:00 2028 GMT
        Attributes: 237 bytes
        Signature Algorithm: sha256WithRSAEncryption
             4a:8f:74:ec:31:c5:52:bb:cc:c5:2c:fc:0c:5f:97:fc:48:77:
             a5:ae:e4:ab:d0:e8:b8:40:23:4b:c0:0c:a5:a3:d3:a2:de:5a:
             08:68:8c:02:45:ff:79:fb:3e:12:50:98:c6:87:2b:81:06:8a:
             16:3f:a2:28:d2:e5:89:e3:7b:48:ec:81:47:75:9e:6f:32:d4:
             48:75:e9:83:de:d7:be:da:26:07:ec:e1:cc:cc:cb:9c:b1:0d:
             cb:eb:79:fe:5c:71:f1:84:da:cc:80:13:86:23:df:bb:43:84:
             67:be:79:bb:38:51:55:a9:22:ad:e6:b5:f4:b1:91:6b:47:5d:
             97:54:3e:bb:08:0d:d5:0b:e9:21:c9:7c:b5:71:5f:f7:bf:de:
             43:c1:61:52:1c:e1:b6:56:48:8a:8c:37:4e:d8:1e:16:46:b2:
             b4:0b:2d:89:ed:91:68:d1:36:2d:68:b3:44:38:d0:01:2f:99:
             df:6b:d3:08:5d:40:20:a3:88:43:c2:1c:4d:49:77:e2:ac:93:
             e0:56:df:07:40:d6:a8:40:f7:a9:1c:38:99:6e:64:59:73:7f:
             10:d4:b0:14:a5:3c:4c:60:37:8f:1f:4a:50:0e:49:88:f5:37:
             64:fb:8f:c2:31:88:54:d0:22:2a:ea:3c:d1:1e:b3:9a:53:07:
             e0:34:6a:7d
```
