# Elementor Loaded

<Badge type="tip" vertical="top" text="Elementor Core" /> <Badge type="warning" vertical="top" text="Basic" />

Elementor has a hook that fires when a plugin is loaded, before loading all the components.

## Hook Details

* **Hook Type:** Action Hook
* **Hook Name:** `elementor/loaded`
* **Affects:** Init Process

## Example

```php
function my_plugin() {

	// ...

}
add_action( 'elementor/loaded', 'my_plugin' );
```
