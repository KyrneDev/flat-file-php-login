# flat-file-php-login

A simple, but secure PHP login script in one file and a flat-file SQLite database.

No installation needed, ready to go in under 60 seconds. Uses the ultra-modern & future-proof PHP 5.5.
BLOWFISH hashing/salting functions (includes the official PHP 5.3 & PHP 5.4 compatibility pack, which makes these
functions available in these versions too). 


## Requirements

- PHP 5.3.7+ (with PDO and SQLite extension activated)

## Installation (quick setup)

Run the install script `_install.php` in the `_installation` folder which will create a `users.db` file (the database).
That's it.

## Important security note

In the default setup the database - which is only a simple users.db file - can be downloaded directly.
To prevent this, change the path of your database file! A path that is not accessable by public is perfect.
The .htaccess in the project only works if you have set `AllowOverride` to `All` in your vhost / apache config.

## Short guide

The `index.php` does all the action, please look into the code for more info, everything is commented. The install script
`_install.php` creates a database (a file named `users.db`) right into the root folder. The `.htaccess` protects your
database file from being downloaded. The `password_compatibility_library.php` is only loaded automatically when you
use a PHP version older than 5.5 to add the new PHP 5.5 password hashing functions to these older PHP versions.
The `_debug.php` is a little helper tool, it simply echoes out the content of the database.

## Useful links

- [How to install SQLite and Ubuntu and Debian](http://www.dev-metal.com/how-to-install-sqlite-driver-for-php-in-ubuntu-debian/)
- [How to use PDO](http://wiki.hashphp.org/PDO_Tutorial_for_MySQL_Developers)
- [A little guideline on how to use the PHP 5.5 password hashing functions and it's "library plugin" based PHP 5.3 & 5.4 implementation](http://www.dev-metal.com/use-php-5-5-password-hashing-functions/)

