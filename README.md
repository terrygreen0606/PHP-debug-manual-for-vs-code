# PHP-debug Manual for vs code.

1. Install Xampp

2. Download php_xdebug-2.7.2-7.3-vc15-x86_64.dll and copy it into xampp/php/ext

3. Add the following content to php.ini file

    [XDebug]
    xdebug.remote_enable=1
    xdebug.remote_autostart=1
    zend_extension = "C:\xampp\php\ext\php_xdebug-2.7.2-7.3-vc15-x86_64 .dll"

4. Restart Apache service.

5. Add the following content to settings.json in vs code.

    "php.validate.executablePath": "c:\\xampp\\php\\php.exe"

6. Install PHP debug extension.

7. Add the following content to launch.json in vs code.

    "version": "0.2.0",
    "configurations": [
        {
            "name": "Listen for XDebug",
            "type": "php",
            "request": "launch",
            "port": 9000
        },
        {
            "name": "Launch currently open script",
            "type": "php",
            "request": "launch",
            "program": "${file}",
            "cwd": "${fileDirname}",
            "port": 9000
        }
]

