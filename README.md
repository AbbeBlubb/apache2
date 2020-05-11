# Configuration for Apache2 web server

## What
- Virtualhost for sharing the same IP-adress with several domain names
- RewriteEngine for serving a single page application where the routing is handled on the client. If the request doesn't match a file or directory, the index.html will be served
- Reactrouter with BrowserRouter handles non-existent routes in the client

## How

- Create the .conf in the sites-available folder
- Enable rewrite (requires restart if to be used immediately)
```
sudo a2enmod rewrite && systemctl restart apache2
```
- Enable site (requires restart)
```
sudo a2ensite example.com.conf && systemctl restart apache2
```
