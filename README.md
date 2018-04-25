# PHP [pre-commit](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)

> GIT pre-commit script appropriate for any PHP project.
> A pre-commit script that validates syntax errors in **PHP**. It also validates PHP files against `PSR2` coding styles.

## About

This is a pre commit script that checks added, copied, modified or renamed files for syntax errors and `PSR2` coding standards.

## Installation

1. `git clone` this repository.
2. Copy the `pre-commit` file to your project's Git hooks folder. Make sure that the `pre-commit` file is executable.

```bash
# Put the pre-commit file in the .git/hooks/ folder in your git repository.
curl -O https://raw.githubusercontent.com/AllysonSilva/php-pre-commit/master/pre-commit

# create new hooks folder
mkdir .git/hooks

# move pre-commit to new hooks folder
mv pre-commit .git/hooks/pre-commit

# don't forget to make the pre-commit file executable
chmod +x .git/hooks/pre-commit
```

## Usage

This will work automatically before every commit.

## [Dependencies](https://github.com/AllysonSilva/environment/blob/master/Composer/composer.json)

### PHP Lint(Syntax check)

A bash script that runs `php -l` against stage files that are php. Assumes `php` is a global executable command. Will exit when it hits the first syntax error.


### [PHP CodeSniffer (PHPMD + PHPCBF)](https://github.com/squizlabs/PHP_CodeSniffer#installation)

> PHP_CodeSniffer is a set of two PHP scripts; the main `phpcs` script that tokenizes PHP, JavaScript and CSS files to detect violations of a defined coding standard, and a second `phpcbf` script to automatically correct coding standard violations. PHP_CodeSniffer is an essential development tool that ensures your code remains clean and consistent.

It will assume that there is a valid PHP Code Sniffer executable at these locations, `vendor/bin/phpcs`, `phpcs` or `php phpcs.phar`.

### [PHP Coding Standards Fixer (PHP-CS-Fixer)](https://github.com/FriendsOfPHP/PHP-CS-Fixer#installation)

> The PHP Coding Standards Fixer (PHP CS Fixer) tool fixes your code to follow standards; whether you want to follow PHP coding standards as defined in the PSR-1, PSR-2, etc., or other community driven ones like the Symfony one.

### [PHP Mess Detector (PHPMD)](https://phpmd.org/download/index.html)

> PHPMD is a spin-off project of PHP Depend and aims to be a PHP equivalent of the well known Java tool PMD. PHPMD can be seen as an user friendly frontend application for the raw metrics stream measured by PHP Depend.

### [PHP Copy/Paste Detector (PHPCPD)](https://github.com/sebastianbergmann/phpcpd)

> `phpcpd` is a Copy/Paste Detector (CPD) for PHP code.

## License

[MIT License](https://github.com/AllysonSilva/php-pre-commit/blob/master/LICENSE)
