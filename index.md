## What is this?
I got fed up of not having a really simple but reliable way to validate public DNS resolution code for things like the DNS resource in (@aelsabbahy's) awesome server validation tool: [goss](https://goss.rocks).

Sure I could use things like google.com or other DNS addresses but I can't guarantee that they won't change or be advertised differently around the globe. The records below are controlled by me and won't ever change. This is also a good exercise for me to get to grips with different DNS server software, logging, filtering, stress testing and protection / security. 

Maybe eventually I'll make some tools available to interact a bit more with DNS (like we need more?).

### What records are available?

#### A Records
```
a.dnstest.io.		3600	IN	A	192.30.252.153
b.dnstest.io.		3600	IN	A	192.30.252.154
```

#### AAAA Records
```
ip6.dnstest.io.		3600	IN	AAAA	2404:6800:4001:807::200e
```

#### CNAME Records
```
c.dnstest.io.		3600	IN	CNAME	a.dnstest.io.
```

#### MX Records
```
dnstest.io.		3600	IN	MX	5 a.dnstest.io.
dnstest.io.		3600	IN	MX	10 b.dnstest.io.
```

#### SRV Records
```
_https._tcp.dnstest.io.	3600	IN	SRV	0 5 443 a.dnstest.io.
_https._tcp.dnstest.io.	3600	IN	SRV	10 10 443 b.dnstest.io.
```

#### TXT Records
```
txt._test.dnstest.io.	3600	IN	TXT	"Hello DNS"
```

#### NS Records
```
dnstest.io.		3600	IN	NS	ns2.dnstest.io.
dnstest.io.		3600	IN	NS	ns1.dnstest.io.
```

#### CAA Records
```
dnstest.io.		3600	IN	CAA	0 issue "comodoca.com"
dnstest.io.		3600	IN	CAA	0 issue "letsencrypt.org"
dnstest.io.		3600	IN	CAA	0 issuewild "\;"
```
