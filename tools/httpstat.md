# httpstat

**Source:** 

- https://github.com/davecheney/httpstat  (Go)
- https://github.com/reorx/httpstat (python)



```bash
$ httpstat 
Usage: httpstat [OPTIONS] URL

OPTIONS:
  -4	resolve IPv4 addresses only
  -6	resolve IPv6 addresses only
  -E string
    	client cert file for tls config
  -H value
    	set HTTP header; repeatable: -H 'Accept: ...' -H 'Range: ...'
  -I	don't read body of request
  -L	follow 30x redirects
  -O	save body as remote filename
  -X string
    	HTTP method to use (default "GET")
  -d string
    	the body of a POST or PUT request; from file use @filename
  -k	allow insecure SSL connections
  -o string
    	output file for body
  -v	print version number

ENVIRONMENT:
  HTTP_PROXY    proxy for HTTP requests; complete URL or HOST[:PORT]
                used for HTTPS requests if HTTPS_PROXY undefined
  HTTPS_PROXY   proxy for HTTPS requests; complete URL or HOST[:PORT]
  NO_PROXY      comma-separated list of hosts to exclude from proxy

```





```bash
 httpstat www.google.es                                              

Connected to 142.250.184.163:443

HTTP/2.0 200 OK
Server: gws
Alt-Svc: h3-29=":443"; ma=2592000,h3-T051=":443"; ma=2592000,h3-Q050=":443"; ma=2592000,h3-Q046=":443"; ma=2592000,h3-Q043=":443"; ma=2592000,quic=":443"; ma=2592000; v="46,43"
Cache-Control: private, max-age=0
Content-Type: text/html; charset=ISO-8859-1
Date: Thu, 25 Feb 2021 17:48:40 GMT
Expires: -1
P3p: CP="This is not a P3P policy! See g.co/p3phelp for more info."
Set-Cookie: NID=210=A0suGR3J44YrUNrIW6hPDGxfbk9xMORLmZD_KkdmAbdU9LLJEV4_gLm1x3O44dF3ZpCzyjacEWWC44Pk49kN4444444444GdA0or4Yc_2ZW5mrLwsk0Jp6XBHeCwtSTERtoWpJR_IG28aE3X64322233cbD_-zoCx23243234A8yzqOA423OyMA; expires=Fri, 27-Aug-2021 17:48:40 GMT; path=/; domain=.google.es; HttpOnly,CONSENT=PENDING+721; expires=Fri, 01-Jan-2038 00:00:00 GMT; path=/; domain=.google.es
X-Frame-Options: SAMEORIGIN
X-Xss-Protection: 0

Body discarded

  DNS Lookup   TCP Connection   TLS Handshake   Server Processing   Content Transfer
[     60ms  |          31ms  |        190ms  |             94ms  |            16ms  ]
            |                |               |                   |                  |
   namelookup:60ms           |               |                   |                  |
                       connect:92ms          |                   |                  |
                                   pretransfer:282ms             |                  |
                                                     starttransfer:377ms            |
                                                                                total:393ms    
```





## Resources

- https://ops.tips/gists/measuring-http-response-times-curl/
- 