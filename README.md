# BAZURL users

Based on the guide at https://fly.io/docs/getting-started/static/

## Custom domain

For a taste of how straightforward the process can be, here’s a speed run for adding a host/domain to an application. Let’s say we have example.com and a Fly app called custom-quartz.

* Run flyctl ips list -a custom-quartz to get the IPv4 and IPv6 addresses.
* Head over to your DNS provider and add A and AAAA records for example.com with the IPv4 and IPv6 values.
* Run flyctl certs create -a custom-quartz example.com
* Run flyctl certs show -a custom-quartz example.com to watch your certificates being issued.
* Connect to https://example.com and use your application with auto-renewing Let’s Encrypt TLS certificates, edge TLS, HTTP/2 support and more. 
