# BAZURL users

Based on the guide at https://fly.io/docs/getting-started/static/

## Custom domain

https://fly.io/blog/how-to-custom-domains-with-fly/
https://fly.io/docs/app-guides/custom-domains-with-fly/

* Run `flyctl ips list` 
  ```
  VERSION IP                      TYPE            REGION  CREATED AT           
  v6      2a09:8280:1::f:a8d2     public          global  2023-11-18T00:01:11Z
  v4      66.241.124.244          public (shared) 
  ``` 
* Update DNS
  Create `A` record with v4 value
  Create `AAAA` record with v6 value
* Run `flyctl certs create user.bazurl.com` to create certificate
* Run `flyctl certs show user.bazurl.com` to verify if certificate is ready

## More
https://fly.io/docs/app-guides/global-nginx-proxy/
