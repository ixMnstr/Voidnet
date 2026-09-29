# Encrypted DNS (AdGuard Home)

VOIDNET uses AdGuard Home on the HP EliteDesk server node to block network-wide tracking and encrypt upstream domain lookups.

## Upstream DNS Configuration
Configured in AdGuard Home under **Settings > DNS Settings**:

```text
# DNS-over-TLS (DoT)
tls://1.1.1.1
tls://1.0.0.1
tls://9.9.9.9

# DNS-over-HTTPS (DoH)
[https://cloudflare-dns.com/dns-query](https://cloudflare-dns.com/dns-query)
[https://dns.quad9.net/dns-query](https://dns.quad9.net/dns-query)
