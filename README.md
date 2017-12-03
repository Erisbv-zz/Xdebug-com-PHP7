# Instale o Xdebug no PHP7.x

* Install Xdebug in PHP7.x
Instale o Xdebug no PHP. Exemplo prático no Xampp.

## Requirements

* Baixe o XAMPP para Windows já com a versão do PHP7.x
* XAMPP for Windows: https://www.apachefriends.org/download.html

## Setup

* Efetue o Download da DLL do XDEBUG
* Download Xdebug for:
  * PHP 7.0.x: https://xdebug.org/files/php_xdebug-2.5.5-7.0-vc14.dll
  * PHP 7.1.x: https://xdebug.org/files/php_xdebug-2.5.5-7.1-vc14.dll
  
* Copy the file: `php_xdebug-2.5.5-7.1-vc14.dll`
* to: `C:\xampp\php\ext`

* Open the file: `C:\xampp\php\php.ini` with Notepad++

* Disable output buffering: `output_buffering = Off`

* Scroll down to the `[XDebug]` section and copy this lines:

```ini
[XDebug]
zend_extension = "c:\xampp\php\ext\php_xdebug-2.5.5-7.1-vc14.dll"
xdebug.remote_autostart = 1
xdebug.profiler_append = 0
xdebug.profiler_enable = 0
xdebug.profiler_enable_trigger = 0
xdebug.profiler_output_dir = "c:\xampp\tmp"
;xdebug.profiler_output_name = "cachegrind.out.%t-%s"
xdebug.remote_enable = 1
xdebug.remote_handler = "dbgp"
xdebug.remote_host = "127.0.0.1"
xdebug.remote_log="c:\xampp\tmp\xdebug.txt"
xdebug.remote_port = 9000
xdebug.trace_output_dir = "c:\xampp\tmp"
; 3600 (1 hour), 36000 = 10h
xdebug.remote_cookie_expire_time = 36000
```

* Stop/Start Apache

* Click on the Github &#9733; Star :-)

## PhpStorm

* Completo Tutorial:
https://confluence.jetbrains.com/display/PhpStorm/Zero-configuration+Web+Application+Debugging+with+Xdebug+and+PhpStorm

* Use the [PhpStorm bookmarklets generator](https://www.jetbrains.com/phpstorm/marklets/) to activate Xdebug from the browser side.

## Netbeans

* Change the Netbeans debugging options: https://postimg.org/image/8tfvemy7l/

## Eclipse

* No comment

## Visual Studio Code

* Install the [PHP Debug Adapter for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=felixfbecker.php-debug).

## Adobe Brackets

* Install the [PHP Debugger for Brackets](https://github.com/spocke/php-debugger).
