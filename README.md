# Let's Encrypt
Min inställning för Let's Encrypt

## Add-on (Hassio) konfigurering

```yaml
keyfile: privkey.pem
certfile: fullchain.pem
challenge: http
dns:
  simply_account_name: XXXXXXX
  simply_api_key: YYYYYYYYYYYYY
  rfc2136_sign_query: true
email: zzzzzzz@zzzz.zzz
domains:
  - hassio.wwwwwww.www
verbose: true
```

## Inställningar i router

Port forwarding

| Service Name | External Port | Internal Port | Internal Address | Protocol |
| --- | --- | --- | --- | --- |
| V-Hassio | 80 | 80 | 192.168.50.80 | TCP |
| V-SSL | 443 | 443 | 192.168.50.80 | TCP |

## Simply DNS Zone

| Type | Hostname | Value | TTL |
| --- | --- | --- | --- |
| A | domain.com | wan-ip | 3600 |
