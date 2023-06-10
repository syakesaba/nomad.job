DNSまわり設定
=============

# レジストラDNSレコード設定例

```
oracle.example.com.       IN   NS   ns1.oracle.example.com.
oracle.example.com.       IN   NS   ns2.oracle.example.com.
ns1.oracle.example.com.   IN   A    IP1
ns1.oracle.example.com.   IN   A    IP2
ns2.oracle.example.com.   IN   A    IP1
ns2.oracle.example.com.   IN   A    IP2
```

# knotdns ゾーン設定例

```
$ORIGIN oracle.example.com.
$TTL 3600
@       SOA     ns1.oracle.example.com. hostmaster.oracle.example.com. (
                2010111213      ; serial
                6h              ; refresh
                1h              ; retry
                1w              ; expire
                1d )            ; minimum

        NS      ns1
        NS      ns2
        A       IP1
        A       IP2

ns1     A       IP1
ns1     A       IP2
ns2     A       IP1
ns2     A       IP2
a       A       IP1
b       A       IP2
```
