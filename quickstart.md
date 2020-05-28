# Multi-Coin Crypto-Payment Gateway

Multi-Coin Crypto-Payment Gateway is a PHP cryptocurrency payment processor based on [BitGo API](https://www.bitgo.com/) which allows you to receive payments in  btc, bch, bsv, btg, dash, ltc, xrp, zec, xlm and ERC20 TOKENS directly on your website with simple integration, with no fees, transaction cost or a middleman.




## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

The Multi-Coin Crypto-Payment Gateway has a few system requirements. you will need to make sure your server meets the following requirements:

- PHP >= 5.6
- MySQL >= 5.5.15
- PDO PHP Extension _(Used to create secure connection to MySQL server.)_
- OpenSSL PHP Extension _(PHP OpenSSL extension must be installed and enabled. This is required for secure data encryption. OpenSSL version must be 1.0.1c or above.)_
- cURL PHP Extension _(Used for making http requests)_
- Multibyte String PHP Extension _(Used for multibyte encoding.)_
- Exif PHP Extension _(optional)_
- Internationalization _(optional)_


To make sure you have everything installed run extra/php_check.php in your browser to see the results.

## Installing

To install Multi-Coin Crypto-Payment Gateway simply read the instructions below.


### 1. Extract files

Extract the files from the archive you have downloaded from CodeCanyon.

### 2. Copy files

Copy the files from the `code` directory to your server. <br> By default the script is set to the main example, but you can install the [other examples](index.md#examples) too.


### 3. Create a database & import the SQL file

Open a database client (phpMyAdmin, etc.), create a new database (and user) and import `database.sql` found in the `code` directory or in the one you copied earlier.

### 4. Configuration

First edit `inc/config.php` and set the database connection details from lines 188.

```JSON

        'database' => 'crypto_box',
        
        /*
        |--------------------------------------------------------------------------
        | Database Username
        |--------------------------------------------------------------------------
        */
        
        'username' => 'root',
        
        /*
        |--------------------------------------------------------------------------
        | Database Password
        |--------------------------------------------------------------------------
        */
        
        'password' => '',
        
        /*
        |--------------------------------------------------------------------------
        | Database Hostname
        |--------------------------------------------------------------------------
        */
        
        'hostname' => 'localhost',

```



Then edit `inc/config.php` and set `url` to the url where the script is located. For example if you have copied the script files into a directory called "payment or checkout" and your website is "http://mywebsite.com" then the `url` should be set to "http://mywebsite.com/payment" or "http://mywebsite.com/checkout".
```JSON
       /*
        |--------------------------------------------------------------------------
        | Website URL
        |--------------------------------------------------------------------------
        | 
        | This URL is used in emails, page redirects and webhook.
        | You must set this to the root of the script without slash full file path
        |
        */

        'url' => 'http://localhost/bitgo-payment',

```


<br>
<br>

Next you should continue with the [BitGo Configuration](bitgo.md) and [BitGo WebHooks](webhooks.md) sections.

<br><br>

See Also
- [BitGo Configuration](bitgo.md)
- [WebHooks](webhooks.md)
- [Restful API](restful.md)
- [Debugging](debugging.md)
