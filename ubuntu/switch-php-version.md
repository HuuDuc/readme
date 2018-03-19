**Environment**

- Ubuntu 16.04
- Apache

----------

## Install PHP version (here: 5.6 and 7.0 or above)

**Install PHP 5.6**

```console
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php5.6 php5.6-mysql php5.6-mbstring libapache2-mod-php5.6
```

**Install PHP 7.0 (or above)**

```console
sudo apt update
sudo apt install php php-mysql php-mbstring libapache2-mod-php
```

----------

## Switch PHP version

**From PHP 7.0 to PHP 5.6**

  - Apache
  ```console
    sudo a2dismod php7.0
    sudo a2enmod php5.6
    sudo service apache2 restart
  ```
  - CLI
  ```console
    sudo update-alternatives --set php /usr/bin/php5.6
  ```

**From PHP 5.6 to PHP 7.0**

  - Apache
  ```console
    sudo a2dismod php5.6
    sudo a2enmod php7.0
    sudo service apache2 restart
  ```
  - CLI
  ```console
    sudo update-alternatives --set php /usr/bin/php7.0
  ```

**Check PHP version**
```console
  php -v
```

Voilà.
