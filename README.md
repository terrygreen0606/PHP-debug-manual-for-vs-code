# PHP-debug Manual for vs code.

1. Install Xampp

2. Go to https://xdebug.org/wizard and copy PHPinfo (of your local computer) content in the textarea.

3. Press the button analyze.

4. Download php_xdebug-2.7.2-7.3-vc15-x86_64.dll and copy it into xampp/php/ext

5. Add the following content to php.ini file

    [XDebug]
    
    xdebug.remote_enable=1
    
    xdebug.remote_autostart=1
    
    zend_extension = "C:\xampp\php\ext\php_xdebug-2.7.2-7.3-vc15-x86_64 .dll"

6. Restart Apache service.

7. Add the following content to settings.json in vs code.

    "php.validate.executablePath": "c:\\xampp\\php\\php.exe" (You have to put double slashes in the path)

8. Install PHP debug extension. (Go to extensions tab in vs-code)

9. Add the following content to launch.json in vs code.

    "version": "0.2.0",
    
    "configurations": 
    
    [
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



