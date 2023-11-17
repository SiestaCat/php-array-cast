# php-array-cast

Install:

```
composer require siestacat/php-array-cast
```

Usage:

```
use Siestacat\PhpArrayCast\Cast;

Cast::class(range(0,9), \stdClass::class); //Will throw error
Cast::class(array_fill(0, 9, new \stdClass), \stdClass::class); //No error

Cast::type(range(0,9), 'string'); //Will throw error
Cast::class(array_fill(0, 9, 'banana'), 'string'); //No error

```


Tests:

```
git clone https://github.com/SiestaCat/php-array-cast.git
cd php-array-cast
composer install
composer run-script test
```
