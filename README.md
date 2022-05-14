## **Here have react js important error fixed code**

### Page not found
> React Links - "requested URL was not found on this server" after being deployed on live server

> _You need to create a file of root directory. The contents of your __.htaccess__ file should be this:_

```bash
RewriteEngine On
RewriteBase /
RewriteRule ^index.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-l
RewriteRule . /index.html [L]
```


## Page not found
> This code need to put at react publish folder directory.

>File name will be > __.htaccess__
```bash
<IfModule mod_rewrite.c>
RewriteEngine On
RewriteBase /
RewriteRule ^index\.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-l
RewriteRule . /index.html [L]
</IfModule>
```