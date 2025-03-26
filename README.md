## Nginx configuration
```shell
rm -rf $(brew --prefix)/etc/nginx
ln -s $(pwd)/nginx $(brew --prefix)/etc/nginx
nginx -t && nginx -s reload
```

## Generate SSL certificate
```shell
# Generate certificate and key files
mkcert -cert-file nginx/ssl/localhost.pem -key-file nginx/ssl/localhost.key \
"*.local.appcloud.lv" "local.appcloud.lv"
```
