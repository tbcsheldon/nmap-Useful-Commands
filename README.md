# nmap-Useful-Commands

Collection of useful nmap commands for penetration testing

## Verbose service/OS scan

```Bash
nmap -p 0-65535 -T4 -A -v [host/IP]
```

## Update scripts
```Bash
nmap --script-updatedb
```

## Banner grabbing
```Bash
nmap -sS -sV -p [Port number] -v -n -Pn --script banner [host/IP]
```

## Vulnerability scanning
```Bash
nmap -sV --script=exploit,external,vuln,auth,default -oX nmap-output.xml --webxml [host/IP]
```

## Vulnerability scanning with CVE detection
https://github.com/vulnersCom/nmap-vulners
https://github.com/scipag/vulscan

```Bash
nmap -sV --script=vulners,vulscan -oX nmap-output.xml --webxml [host/IP]
```


### More to follow
WAF's might disrupt these commands, I will be updating this repo with commands to rate limit and spoof MAC & IP address' to get around this
