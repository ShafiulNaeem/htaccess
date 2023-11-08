```PHP
  <IfModule mod_rewrite.c>
      <IfModule mod_negotiation.c>
          Options -MultiViews
      </IfModule>
  
      RewriteEngine On
  
      # Redirect Trailing Slashes If Not A Folder...
      RewriteCond %{REQUEST_FILENAME} !-d
      RewriteRule ^(.*)/$ /$1 [L,R=301]
  
      # Handle Front Controller...
      RewriteCond %{REQUEST_FILENAME} !-d
      RewriteCond %{REQUEST_FILENAME} !-f
      RewriteRule ^ index.php [L]
  
      # Handle Authorization Header
      RewriteCond %{HTTP:Authorization} .
      RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]
  </IfModule>
``
