# Custom Post Type Helper Class

## Installation

`composer require Horttcore\CustomPostType`

## Usage

Extend the abstract class `Horttcore\CustomPostType\PostType()` and overwrite following methods:

* `getConfig()`
* `getLabels()`
* `getPostUpdateMessage( \WP_Post $post, string $postType, \WP_Post_Type $postTypeObjects )`

The extending class _MUST_ define protected class variable `slug`

## Example

```php
<?php
use Horttcore\CustomPostType\PostType;

class Things extends PostType
{

	protected $slug = 'thing';

	function getConfig(): array
	{
		return [

		];
	}

	function getLabels(): array
	{
		return [

		];
	}

	function getPostUpdateMessage(): array
	{
		return [

		];
	}
}
```

## Changelog

### v1.0.1

* Fix typos

### v1.0.0

* Initial release