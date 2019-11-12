#### Download Screenshot

```bash
jeff@debian:~/Downloads/scratch/instguid.git$ curl -sSL https://raw.githubusercontent.com/hyperledger/fabric/master/scripts/bootstrap.sh | bash -s -- 1.4.0
bash: line 181: [: too many arguments

Installing hyperledger/fabric-samples repo

===> Checking out v1.4.0 of hyperledger/fabric-samples
HEAD is now at bb39b6e... [FAB-13570] Align fabric-samples with 1.4.0 release

Installing Hyperledger Fabric binaries

===> Downloading version 1.4.0 platform specific fabric binaries
===> Downloading:  https://nexus.hyperledger.org/content/repositories/releases/org/hyperledger/fabric/hyperledger-fabric/linux-amd64-1.4.0/hyperledger-fabric-linux-amd64-1.4.0.tar.gz
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 50.9M  100 50.9M    0     0  78802      0  0:11:17  0:11:17 --:--:-- 45874
==> Done.
===> Downloading version 1.4.0 platform specific fabric-ca-client binary
===> Downloading:  https://nexus.hyperledger.org/content/repositories/releases/org/hyperledger/fabric-ca/hyperledger-fabric-ca/linux-amd64-1.4.0/hyperledger-fabric-ca-linux-amd64-1.4.0.tar.gz
==> Partial binary file found. Resuming download...
==> File downloaded. Verifying the md5sum...
==> Extracting hyperledger-fabric-ca-linux-amd64-1.4.0.tar.gz...
==> Done.

Installing Hyperledger Fabric docker images

===> Pulling fabric Images
==> FABRIC IMAGE: peer

1.4.0: Pulling from hyperledger/fabric-peer
3b37166ec614: Pull complete
504facff238f: Pull complete
ebbcacd28e10: Pull complete
c7fb3351ecad: Pull complete
2e3debadcbf7: Pull complete
fc435e46e32e: Pull complete
a4922bafdce8: Pull complete
7d9964965066: Pull complete
625153a09c48: Pull complete
291344806a10: Pull complete
Digest: sha256:9707c97f787de1d4d6dd60994d6b8ea2e5cc28b0f42e6849df3fb41c64b41372
Status: Downloaded newer image for hyperledger/fabric-peer:1.4.0
==> FABRIC IMAGE: orderer

1.4.0: Pulling from hyperledger/fabric-orderer
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
7d9964965066: Already exists
1aa1f5822ea4: Pull complete
f3adcb95411e: Pull complete
Digest: sha256:644265186b4887c7d9dcb91895124ccead3c0125c2c4f9eadc421dc9555d7495
Status: Downloaded newer image for hyperledger/fabric-orderer:1.4.0
==> FABRIC IMAGE: ccenv

1.4.0: Pulling from hyperledger/fabric-ccenv
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Pull complete
33f930d7053e: Downloading [==========>                                        ]  26.31MB/127.5MB
33f930d7053e: Pull complete
7aa21e006739: Pull complete
806ba27e29bb: Pull complete
0292b0ff822a: Pull complete
5d4ce0f5fd82: Pull complete
3bde20c14104: Pull complete
Digest: sha256:6d797cac9fd39d4c9964fbcf02e47137ce8ae321af60832c41d511f0c7ed4d3e
Status: Downloaded newer image for hyperledger/fabric-ccenv:1.4.0
==> FABRIC IMAGE: javaenv

1.4.0: Pulling from hyperledger/fabric-javaenv
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Already exists
33f930d7053e: Already exists
7aa21e006739: Already exists
806ba27e29bb: Already exists
af7eebe5d909: Pull complete
c0ad74369a8f: Pull complete
e36a0232c697: Pull complete
c44da90e9317: Pull complete
91686ed50f7f: Pull complete
1bc0e6d0fb0f: Pull complete
db373eca3e52: Pull complete
942e34fe9650: Pull complete
e49b8e9d853d: Pull complete
094ba7d3af94: Pull complete
4bf56bdf76e0: Pull complete
138eeaa643a0: Pull complete
2b405cbef2dc: Pull complete
386086ff2840: Pull complete
32bb4435cb82: Pull complete
3280cfa711dc: Pull complete
6b14cff5081c: Pull complete
04743de5a814: Pull complete
5360864ccda4: Pull complete
2fd4fc8d8137: Pull complete
bd0e3b20a1bb: Pull complete
a298ecbfeab2: Pull complete
c7b9277c5a65: Pull complete
201919c3a1fe: Pull complete
539bfc561087: Pull complete
4e779849c7ea: Pull complete
3a7304a5b624: Pull complete
Digest: sha256:f392f0c568e515b3e14c9afce14340ba18bc456cfd831ffcb4f72db58dbbcc34
Status: Downloaded newer image for hyperledger/fabric-javaenv:1.4.0
==> FABRIC IMAGE: tools

1.4.0: Pulling from hyperledger/fabric-tools
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Already exists
33f930d7053e: Already exists
7aa21e006739: Already exists
806ba27e29bb: Already exists
72b2b3c78600: Pull complete
f36a6f470154: Pull complete
19fc6d1044df: Pull complete
Digest: sha256:aee256916d0cb938d8023fa32ed2745991d32cfe79018e360f1720707ebfbdb5
Status: Downloaded newer image for hyperledger/fabric-tools:1.4.0
===> Pulling fabric ca Image
==> FABRIC CA IMAGE

1.4.0: Pulling from hyperledger/fabric-ca
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
c8ec0cae397c: Pull complete
3153e2e7116e: Pull complete
d84abf263d15: Pull complete
45ff112943d3: Pull complete
c4678d50bc7a: Pull complete
Digest: sha256:c1dce534d9e9202697e0aaad7c5521d958700fda0b05127dafb9333c22e15f74
Status: Downloaded newer image for hyperledger/fabric-ca:1.4.0
===> Pulling thirdparty docker images
==> THIRDPARTY DOCKER IMAGE: couchdb

0.4.14: Pulling from hyperledger/fabric-couchdb
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Already exists
33f930d7053e: Already exists
7aa21e006739: Already exists
806ba27e29bb: Already exists
36861d712d08: Pull complete
d90f5e3e2060: Pull complete
24997f7eee08: Pull complete
3178b1827d0f: Pull complete
7483b6e6320e: Pull complete
3ca8322e6d72: Pull complete
e3f87c16fd0e: Pull complete
fa9f1a1e037c: Pull complete
08b197ff3973: Pull complete
ed0c2b2f2e3e: Pull complete
Digest: sha256:021c7e4a5047432d892fbdf7d5220d3049ff4e8b436fd481bb08e41871f1aac7
Status: Downloaded newer image for hyperledger/fabric-couchdb:0.4.14
==> THIRDPARTY DOCKER IMAGE: kafka

0.4.14: Pulling from hyperledger/fabric-kafka
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Already exists
33f930d7053e: Already exists
7aa21e006739: Already exists
806ba27e29bb: Already exists
5b93606e43dd: Pull complete
c28e9396b3a9: Pull complete
d4fac70bff73: Pull complete
Digest: sha256:82ac81938320d05a538b9fd6de0fcd54b5a999188cf9b08822cf25f9ad7970a9
Status: Downloaded newer image for hyperledger/fabric-kafka:0.4.14
==> THIRDPARTY DOCKER IMAGE: zookeeper

0.4.14: Pulling from hyperledger/fabric-zookeeper
3b37166ec614: Already exists
504facff238f: Already exists
ebbcacd28e10: Already exists
c7fb3351ecad: Already exists
2e3debadcbf7: Already exists
fc435e46e32e: Already exists
a4922bafdce8: Already exists
14675a1189ca: Already exists
33f930d7053e: Already exists
7aa21e006739: Already exists
806ba27e29bb: Already exists
04fff5ccfdcb: Pull complete
dbe82feb14ae: Pull complete
ba7a23bea382: Pull complete
5f6e0d1bbcbd: Pull complete
Digest: sha256:ac342ed87997175bfd557c53f7ffc6e0f8aa32bcaebb54a9bd55fb4c7f954802
Status: Downloaded newer image for hyperledger/fabric-zookeeper:0.4.14

===> List out hyperledger docker images
hyperledger/fabric-javaenv     1.4.0               3d91b3bf7118        7 days ago          1.75GB
hyperledger/fabric-javaenv     latest              3d91b3bf7118        7 days ago          1.75GB
hyperledger/fabric-tools       1.4.0               0a44f4261a55        11 days ago         1.56GB
hyperledger/fabric-tools       latest              0a44f4261a55        11 days ago         1.56GB
hyperledger/fabric-ccenv       1.4.0               5b31d55f5f3a        11 days ago         1.43GB
hyperledger/fabric-ccenv       latest              5b31d55f5f3a        11 days ago         1.43GB
hyperledger/fabric-orderer     1.4.0               54f372205580        11 days ago         150MB
hyperledger/fabric-orderer     latest              54f372205580        11 days ago         150MB
hyperledger/fabric-peer        1.4.0               304fac59b501        11 days ago         157MB
hyperledger/fabric-peer        latest              304fac59b501        11 days ago         157MB
hyperledger/fabric-ca          1.4.0               1a804ab74f58        11 days ago         244MB
hyperledger/fabric-ca          latest              1a804ab74f58        11 days ago         244MB
hyperledger/fabric-zookeeper   0.4.14              d36da0db87a4        3 months ago        1.43GB
hyperledger/fabric-zookeeper   latest              d36da0db87a4        3 months ago        1.43GB
hyperledger/fabric-kafka       0.4.14              a3b095201c66        3 months ago        1.44GB
hyperledger/fabric-kafka       latest              a3b095201c66        3 months ago        1.44GB
hyperledger/fabric-couchdb     0.4.14              f14f97292b4c        3 months ago        1.5GB
hyperledger/fabric-couchdb     latest              f14f97292b4c        3 months ago        1.5GB
```
