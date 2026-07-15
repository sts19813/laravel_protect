# Laravel Protect

Archivos `.htaccess` para instalaciones de Laravel donde el proyecto completo se encuentra dentro de `public_html` y la aplicación debe servirse exclusivamente desde `public/`.

## Instalación

Coloca los archivos del repositorio en estas ubicaciones:

```text
public_html/.htaccess
public_html/public/.htaccess
```

## Permisos y caché de Laravel

Desde la raíz del proyecto ejecuta:

```bash
chmod 600 .env
chmod 644 .htaccess

php artisan optimize:clear
php artisan config:cache
php artisan view:cache
```

## Hostinger con PHP 8.5

Si el comando `php` de la terminal usa una versión anterior, ejecuta Artisan mediante el binario PHP 8.5 de Hostinger:

```bash
/opt/alt/php85/usr/bin/php artisan optimize:clear
/opt/alt/php85/usr/bin/php artisan config:cache
/opt/alt/php85/usr/bin/php artisan view:cache
```

Comprueba la versión disponible con:

```bash
/opt/alt/php85/usr/bin/php -v
```
