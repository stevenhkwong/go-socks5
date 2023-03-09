
This is the first of my private branch.
The original forked branch in github is the master.

Not very good original README so here's more info:


INFO
-----
The default port is 10800
The RFC rfc1928 port for socks5 proxy is 1080
To use the example code change it in
    _example/main.go


START
=====
To start:
go run _example/main.go 

TEST with:
==========


Test with nc
------------
start a nc listener on wong-gate-2:
nc -kl 4444
hit it thru the socks proxy:
nc --proxy-type socks5 --proxy localhost:10800 wong-gate-2.home 4444

Test with ssh
-------------



Test http
---------
This works so does it mean it is accepting CONNECT ?
-----------------------------------------------------
curl -k -v -socks5 localhost:10800 https://www.wongsrus.net
