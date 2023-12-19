GohostingCAMP Twig Extensions
=======================

A number of useful filters for Twig.

## Installation

GohostingCAMP's Twig Extensions can be easily installed using [composer](http://getcomposer.org/)

    composer require gohostingcamp/twig-extensions

## Usage

```php
$twig = new Twig_Environment($loader, $options);
$twig->addExtension(new GohostingCAMP\Twig\html_entity_decodeExtension());
```

To use in a symfony project [register the extensions as a service](http://symfony.com/doc/current/cookbook/templating/twig_extension.html#register-an-extension-as-a-service).

```yaml
services:
  twig.extension.html_entity_decode:
    class: GohostingCAMP\Twig\html_entity_decodeExtension
    tags:
      - { name: twig.extension }

```


## html_entity_decode extension

```
{{ client.fullname|html_entity_decode }}
```


## Utf8_ansi extension

```
{{ client.fullname|Utf8_ansi }}
```
