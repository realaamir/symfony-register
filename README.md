# Author

-   @Aamir Shaikh
-   Submission Date: 25th Nov 2023

# Challenge

-   We are given with a challenge to create a Registration form using symfony framework.

# Pre-Requisite

-   PHP: 8.1 and higher
-   MySQL: 5.0 or higher
-   Web Server (eg: Apache, Nginx, IIS)
-   [Other libraries](https://symfony.com/doc/current/index.html)

# My Solution

-   Install Symfony framework.
-   Created user registration form with email and password validation.
-   Created login session using symfony default system.

## Framework

PHP uses [Symfony](https://symfony.com/doc/current/index.html), the best existing PHP framework, as the foundation framework and [Module](https://symfony.com/doc/current/index.html) package for Apps.

## Installation

-   Install [Composer](https://getcomposer.org/download)
-   Clone the repository: `git clone https://github.com/realaamir/symfony-register.git`
-   Install dependencies: `composer install ;`


```bash
php bin/console doctrine:migrations:diff
php bin/console doctrine:migrations:migrate
php bin/console cache:clear
php -S localhost:3000 -t public
```

# Usage

## Create User

```
(http://localhost:3000/register)
(http://localhost:3000/login)
Validation Check: Email should be unique, Password should be alphanumeric.
```


# License

MIT
