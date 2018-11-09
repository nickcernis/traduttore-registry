# Traduttore Registry


[![Build Status](https://travis-ci.com/wearerequired/traduttore-registry.svg?branch=master)](https://travis-ci.com/wearerequired/traduttore-registry) [![codecov](https://codecov.io/gh/wearerequired/traduttore-registry/branch/master/graph/badge.svg)](https://codecov.io/gh/wearerequired/traduttore-registry)

Allows loading translation files from a custom GlotPress site running [Traduttore](https://github.com/wearerequired/traduttore).

## Installation

If you're using [Composer](https://getcomposer.org/) to manage dependencies, you can use the following command to add the plugin to your site:

```bash
composer require wearerequired/traduttore-registry
```

After that, you can use `Required\Traduttore_Registry\add_project( $type, $slug, $api_url )` in your theme or plugin. On a multisite install, it's recommend to use it in a must-use plugin.

## Usage

Here's an example of how you can use that function:

```php
\Required\Traduttore_Registry\add_project(
	'plugin',
	'example-plugin',
	'https://translate.example.com/api/translations/acme/acme-plugin/'
);

\Required\Traduttore_Registry\add_project(
	'theme',
	'example-theme',
	'https://translate.example.com/api/translations/acme/acme-theme/'
);
```
