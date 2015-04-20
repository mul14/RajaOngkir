# RajaOngkir.com Shipping PHP library

## Usage

From your terminal

```sh
composer require nasution/rajaongkir
```

Add this to your PHP code

```php
<?php

require 'vendor/autoload.php';

use Nasution\Shipping\RajaOngkir\Endpoints as RajaOngkir;

$apiKey = 'YOUR_API_KEY';
$accountType = 'starter'; // starter or basic

$rajaongkir = new RajaOngkir($apiKey, $accountType);

// Fetch all provinces data
$rajaongkir->provice();

// Fetch specific province
$rajaongkir->provice(5);

// Fetch all cities
$rajaongkir->city();

// Fetch city by province
$rajaongkir->city($provinceId = 5);

// Fetch specific city
$rajaongkir->city($provinceId = 5, $cityId = 501);

// Get the cost
$rajaongkir->cost(
    $fromCityId = 501, 
    $toCityId = 278, 
    $weightInGram = 1000, 
    $courierId = 'jne'; // jne, tiki, pos
);
```

## References

- http://rajaongkir.com/dokumentasi
- https://github.com/hok00age/rajaongkir-codeigniter

## License: Unknown

Ask him https://github.com/hok00age
