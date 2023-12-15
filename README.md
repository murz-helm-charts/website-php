# website-php
This is a Helm chart to deploy a regular website using a PHP engine, like
Drupal CMS, Symfony, WordPress, Laravel.

It uses a single container approach where Nginx and PHP-FPM work in one
container, using the [fpm-nginx](https://github.com/bkuhl/fpm-nginx) container.

To deploy a website you need just two steps:

1. Copy the website files to the `/website` directory on the website PVC.

2. Copy database data to the database PVC.

And that's it.

The DB access credentials will be available in the website container via
environment variables:

- DATABASE_TYPE
- DATABASE_HOST
- DATABASE_NAME
- DATABASE_PASSWORD
- DATABASE_USERNAME
