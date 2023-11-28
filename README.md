﻿# Author

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

-   Install [Composer](https://getcomposer.org/download) and [Npm](https://nodejs.org/en/download)
-   Clone the repository: `git clone https://github.com/akaunting/akaunting.git`
-   Install dependencies: `composer install ;`


```bash
php bin/console doctrine:migrations:diff
```


# Usage

## Create Customer

```

Set Header
- `Authorization: "Bearer <Access Token>"`

POST http://localhost/akaunting/api/customer

Body
{
    "type":"customer",
    "name":"aamir",
    "email":"aamira6@gmil.com",
    "currency_code":"USD"
}

Validation Check: Name and Email should be unique.
```

## Create Invoice and Billing

```
Set Header
- `Authorization: "Bearer <Access Token>"`

POST http://localhost/akaunting/api/invoice

Body
{
    "document_number":"BILL-00005",
    "type":"bill",
    "status":"sent",
    "issued_at":"2023-09-20 15:23:05",
    "due_at":"2023-09-20 15:23:05",
    "amount":"200.23",
    "contact_id":"1",
    "contact_name":"aamir",
    "category_id":"2",
    "currency_code":"USD",
    "currency_rate":"1"
}

Validation Check: Document number should be unique.
Default values for parameters
type - invoice or bill
status - sent and draft (use sent as email is not integrated )
issued_at - whatever the time of creation for invoice or bill
due_at - whatever the due date of for invoice or bill
amount - whatever the amount of for invoice or bill
contact_id - it is the customer to whom we want to send invoice or bill
category_id - 1 (Transfer), 2 (Deposite)
currency_code - Use currency code that we are using it will be dynamic from the get currency api
currency_rate - currenct currency rate that we have define in database, for that we have api by default

```

# Files and changes

For routing [routes](https://github.com/realaamir/akaunting/blob/main/routes/api.php)
For Controller [Customer](https://github.com/realaamir/akaunting/blob/main/app/Http/Controllers/Api/Sales/Customers.php) and [Invoice/Billing](https://github.com/realaamir/akaunting/blob/main/app/Http/Controllers/Api/Sales/Invoices.php)

# License

MIT
