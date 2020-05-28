
- [Ajax Errors](#ajax-errors)
- [Error Handling](#error-handling)

To enable error reporting make sure the `debug` mode is set to `true` in `inc/config.php`. <br> Also make sure you have the errors turned on in your PHP config file (php.ini).

## Ajax Errors

If you get an unexpected error (_Oops! Something went wrong._), you can use browser dev tools to see the errors and response from the server.

In Google Chrome, right-click and select __Inspect__, or use the keyboard shortcut: <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>I</kbd> (or <kbd>Cmd</kbd>+<kbd>Opt</kbd>+<kbd>I</kbd> on Mac).

Navigate to the __Console__ tab to see potential JavaScript errors and the __Network__ tab to see the requests/responses when you upload files (make sure _Record Network_ Log is on). 

If you get errors about the "Request Origin" request make sure you accept the request in `ajax.php` from where you send it by adding:
 
```php
header('Access-Control-Allow-Origin: yourwebsite.com');
header('Access-Control-Allow-Origin: www.yourwebsite.com');
```

## Error Handling 

Multi-Coin Crypto-Payment Gateway comes with a <a href="https://github.com/filp/whoops" target="_blank">whoops</a> error handling. However, if you want to disable it open `inc/init.php` search for "_Register Custom Exception Handling_" and delete/comment this line:

```php
	/*
	|--------------------------------------------------------------------------
	| Set PHP Error Reporting
	|--------------------------------------------------------------------------
	*/
    startExceptionHandling($whoops);
```