Drupal Docker Utils


# Available

## PHPCS

Check current folder against Drupal Coding standards:
```
docker run --rm -ti -v $(pwd):/var/www/html zaporylie/phpcs
```

## SSHD

Get access to /var/www/html from another php container:
```
docker run -dP --volumes-from=<your-php-container> zaporylie/sshd
```
