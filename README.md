# PHP based micro service coding standards

This page list all agreed coding standards adopted at EncoreTickets for each PHP based micro services.

Anyone can suggest a change for this page by submitting a Github pull requests that will need to be discussed and voted by all current developers in order to obtain an agreement by the majority.

## Naming Conventions

This section is talking about the adopted naming conventions.

#### Interface, Class, Exception, Traits naming: 
- Prefix abstract classes with ***Abstract***;
- Suffix interfaces with ***Interface***;
- Suffix traits with ***Trait***;
- Suffix exceptions with ***Exception***;

## Coding style

This section is talking about the adopted coding styles, we're currently using PHP-CS-FIXER to detect any violation of the following rules

### @Symfony set rules.

The list can be found here [PHP-CS-Fixer](https://github.com/FriendsOfPHP/PHP-CS-Fixer)

### array_syntax = short

```php
// Before
array('value');

// Now
['value'];
```

### declare_strict_types = true

Force strict types declaration in all files. Requires PHP >= 7.0.

Risky rule: forcing strict types will stop non strict code from working.

```php
<?php

declare(strict_types=1);
```

### Class (Namespace) naming

Use camel case for each separate semantic unit, including abbreviation, e.g.:
XI -> Xi
Data Transfer Object -> DTO -> Dto

Classes:
- TT API -> TtApi
- US Tax -> UsTax
NOTE: we still have E.API that usually understood as Entertain API that's why EApi

Namespases:
- App\Dto\Item
- App\Gateway\TtApi

