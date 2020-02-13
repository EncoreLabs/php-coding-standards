# PHP based micro service coding standards

This page list all agreed coding standards adopted at EncoreTickets for each PHP based micro services.

Anyone can suggest a change for this page by submitting a Github pull requests that will need to be discussed and voted by all current developers in order to obtain an agreement by the majority.

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