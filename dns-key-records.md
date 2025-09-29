# DNS Key Records

### A Record
Maps a hostname to an IPv4 address.

### AAAA Record
Similar to an A record, but maps to an IPv6 address.

### CNAME 
Stands for Canonical Name and it creates an alias, pointing one hostname to another hostname, never to an IP address. Common use cases are subdomains. When you visit my blog, dyeadal.blogspot.com your computer resolves a CNAME record which then tells your computer to resolve the domain "blogspot[.]com" which will be an A or AAAA record to direct your traffic to their root domain's IP address.

Results for CNAME record above:

| Type  | Domain Name      | TTL | Canonical Name                   |
| ----- | ---------------- | --- | -------------------------------- |
| CNAME | dyeadal.blogspot | 300 | blogspot.l.googleusercontent.com |


Your computer then tries to resolve `blogspot.l.googleusercontent.com` which then returns an A or AAAA record. You can see this in action by using the `dig` command. Below you can see that it resolved to an A record of `142.250.114.132`

```sh
dyeadal@localhost $ dig dyeadal@blogspot.com

...
;; QUESTION SECTION:
;dyeadal.blogspot.com.		IN	A

;; ANSWER SECTION:
dyeadal.blogspot.com.	300	IN	CNAME	blogspot.l.googleusercontent.com.
blogspot.l.googleusercontent.com. 300 IN A	142.250.114.132
...
```


### MX Record
Specifies mail servers responsible for accepting email on behalf of the domain. The LOWER the number, the HIGHER the priority. 
LOWER == HIGHER
[Cloudflare Learning Article - What is a DNS MX record?](https://www.cloudflare.com/learning/dns/dns-records/dns-mx-record/)
[MX Toolbox Online Tool - View a domain's MX records in priority order](https://mxtoolbox.com/)

### TXT Record
Record used for various purposes, including email security information like SPF (lists authorized servers that can send email from that domain), DKIM (specifically the public key for digitally signed emails), and DMARC (how to handle SPF and DKIM policy failures) that help prevent email spoofing and domain verification.
[Cloudflare Learning Article -  DNS TXT records](https://www.cloudflare.com/learning/dns/dns-records/dns-txt-record/)

### NS Record:
Stands for Name Server, it redirects the DNS resolution to another DNS server, to delegate DNS resolution authority to another authoritative DNS server.
[Cloudflare Learning Article - DNS NS record](https://www.cloudflare.com/learning/dns/dns-records/dns-ns-record/)
