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

### no_superfluous_phpdoc_tags = true

  Removes ``@param`` and ``@return`` tags that don't provide any useful information.

```php

// Before

    /**
     * @param string $name
     * @param int $weight
     */
    public function __construct(
        string $name,
        int $weight
    ) {
        $this->name = $name;
        $this->weight = $weight;
    }

// After

    public function __construct(
        string $name,
        int $weight
    ) {
        $this->name = $name;
        $this->weight = $weight;
    }
```