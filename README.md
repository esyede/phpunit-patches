# phpunit-patches
Patch untuk PHPUnit 4.8.34 agar tetap bisa dipakai di PHP 5.3 sampai PHP 8.




Contoh konfigurasi composer:

```json
{
    "require-dev": {
        "cweagans/composer-patches": "^1.7",
        "phpunit/phpunit": "4.8.34"
    },
    "extra": {
        "composer-exit-on-patch-failure": true,
        "patches": {
            "phpunit/phpunit-mock-objects": {
                "Fix PHP 7 and 8 compatibility": "https://cdn.jsdelivr.net/gh/esyede/phpunit-patches/phpunit_mock_objects.patch"
            },
            "phpunit/php-file-iterator": {
                "Fix PHP 8.1 compatibility": "https://cdn.jsdelivr.net/gh/esyede/phpunit-patches/phpunit_path_file_iterator.patch"
            },
            "phpunit/phpunit": {
                "Fix PHP 7 compatibility": "https://cdn.jsdelivr.net/gh/esyede/phpunit-patches/phpunit_php7.patch",
                "Fix PHP 8 compatibility": "https://cdn.jsdelivr.net/gh/esyede/phpunit-patches/phpunit_php8.patch",
                "Fix PHP 8.1 compatibility": "https://cdn.jsdelivr.net/gh/esyede/phpunit-patches/phpunit_php81.patch"
            }
        }
    }
}
```
