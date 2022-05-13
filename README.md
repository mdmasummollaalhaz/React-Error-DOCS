## **Here have react js important error fixed code**

> React Links - "requested URL was not found on this server" after being deployed on live server

> _You need to create a file of root directory. The contents of your .htacces file should be this:_

```bash
RewriteEngine On
RewriteBase /
RewriteRule ^index.html$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteCond %{REQUEST_FILENAME} !-l
RewriteRule . /index.html [L]
```