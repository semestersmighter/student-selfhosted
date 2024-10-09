---
title: self hosted tips
toc: false
---

This is the landing page.

## Explore

{{< cards >}}
  {{< card link="docs" title="Docs" icon="book-open" >}}
  {{< card link="about" title="About" icon="user" >}}
{{< /cards >}}

## Documentation

```bash {filename="db.home.me"}
;
; BIND data file for example.com
;
$TTL    604800
@       IN      SOA     ns.home.me. admin.home.me. (
                      1         ; Serial
                 604800         ; Refresh
                  86400         ; Retry
                2419200         ; Expire
                 604800 )       ; Negative Cache TTL
;
@       IN      NS      ns.home.me.
ns      IN      A       10.0.0.5
@       IN      A       10.0.0.5
www     IN      A       10.0.0.5
web     IN      A       10.0.0.6
```