# ohmyns

## Usage

```shell
dig +short help.ohmyns.com txt
  "makefragment; fragment; cname; ttl; sleep; black; white; echo; log"
```

```shell
dig +short makefragment.help.ohmyns.com txt
  "usage: dig +short txt makefragment-1480_suffix-random.help.ohmyns.com"

dig +short txt makefragment-1480_suffix-random.help.ohmyns.com
  "fragment-001-007-178-178-062-010-020-030-4096-random000.trace.ohmyns.com"
```

```shell
dig +short cname.help.ohmyns.com txt
  "example: dig cname-subdomain.trace.ohmyns.com"

dig cname-subdomain.trace.ohmyns.com
  ;; ANSWER SECTION:
  cname-subdomain.trace.ohmyns.com. 0 IN	CNAME	subdomain.trace.ohmyns.com.
  subdomain.trace.ohmyns.com. 0	IN	A	39.107.97.203
```

```shell
dig ttl-20_cname-random.trace.ohmyns.com
  ;; ANSWER SECTION:
  ttl-20_cname-random.trace.ohmyns.com. 19 IN CNAME random.trace.ohmyns.com.
  random.trace.ohmyns.com. 0	IN	A	39.107.97.203

dig cname-subdomain.trace.ohmyns.com
  ;; ANSWER SECTION:
  cname-subdomain.trace.ohmyns.com. 0 IN	CNAME	subdomain.trace.ohmyns.com.
  subdomain.trace.ohmyns.com. 0	IN	A	39.107.97.203
```

```shell
dig +short random-1.echo.ohmyns.com txt @8.8.8.8
  "query: random-1.echo.ohmyns.com, resolver: 74.125.186.79:43785, txid: 40033"
```

```shell
dig random-1_log.trace.ohmyns.com

curl https://ohmyns.com/dns/resolver/trace\?domain\=random-1_log.trace.ohmyns.com                       
  {"success":true,"message":null,"resolverIP":"74.125.80.139","clientIP":"221.218.171.75","timestamp":"2018-10-19T15:15:08.319+0000"}
```
