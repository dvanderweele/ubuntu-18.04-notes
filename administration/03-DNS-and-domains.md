# DNS & Domain Name Setup
## Administration

In your domain name settings for domain 'xyz.net' in your registrar account, an A record with hostname 'nextcloud' and value of ip address xxx.xxx.xxx.xxx will create the following url that targets the xxx.xxx.xxx.xxx ip address:
```
nextcloud.xyz.net
```
A command to test if the dns has propagated for the domain above:
```bash
nslookup nextcloud.xyz.net
```

