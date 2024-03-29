# PHP-debug Manual for vs code.

### Windows
1. Install Xampp and copy PHP.info page.

2. Go to https://xdebug.org/wizard and paste the PHPinfo (of your local computer) content in the textarea.

3. Press the button analyze.

4. Download php_xdebug-2.7.2-7.3-vc15-x86_64.dll and copy it into xampp/php/ext

5. Add the following content to php.ini file
    ```js
    [XDebug]
    xdebug.mode = debug
    xdebug.start_with_request = yes
    xdebug.client_port = 9000
    zend_extension = "C:\xampp\php\ext\php_xdebug-2.7.2-7.3-vc15-x86_64 .dll"
    ```

6. Restart Apache service.

7. Add the following content to settings.json in vs code.

    ```js
    "php.validate.executablePath": "c:\\xampp\\php\\php.exe"
    ```

8. Install PHP debug extension. (Go to extensions tab in vs-code)

9. Add launch.json in vs code.

### Ubuntu (linux)
Add xdebug configuration in both /opt/lampp/etc/php.ini and /etc/php/{version}/cli/php.ini

## Additional Points
Add this to ignore vendor files in launch.json
```js
"ignore": [
    "**/vendor/**/*.php"
]
```


