# Registering Widgets

<Badge type="tip" vertical="top" text="Elementor Core" /> <Badge type="warning" vertical="top" text="Intermediate" />

When you create new [Elementor widgets](./../widgets/), you must register them. This is done by hooking to the registration hook in the widgets manager and passing a new widget instance.

## Registering New Widgets

As of Elementor 3.5, developers should use the following code to register new widgets:

```php
/**
 * Register new Elementor widgets.
 *
 * @param \Elementor\Widgets_Manager $widgets_manager Elementor widgets manager.
 * @return void
 */
function register_new_widgets( $widgets_manager ) {

	require_once( __DIR__ . '/widgets/widget-1.php' );
	require_once( __DIR__ . '/widgets/widget-2.php' );

	$widgets_manager->register( new \Elementor_Widget_1() );
	$widgets_manager->register( new \Elementor_Widget_2() );

}
add_action( 'elementor/widgets/register', 'register_new_widgets' );
```

This hooks to the `elementor/widgets/register` action hook which holds the widgets manager. The manager then registers new widgets by passing the widget instance.

## Registering New Widgets in Previous Versions

For earlier versions, prior to Elementor 3.5, register new widgets using the following code:

```php
/**
 * Register new Elementor widgets.
 *
 * @param \Elementor\Widgets_Manager $widgets_manager Elementor widgets manager.
 * @return void
 */
function register_new_widgets( $widgets_manager ) {

	require_once( __DIR__ . '/widgets/widget-1.php' );
	require_once( __DIR__ . '/widgets/widget-2.php' );

	$widgets_manager->register_widget_type( new \Elementor_Widget_1() );
	$widgets_manager->register_widget_type( new \Elementor_Widget_2() );

}
add_action( 'elementor/widgets/widgets_registered', 'register_new_widgets' );
```

This hooks the `elementor/widgets/widgets_registered` action hook and passes a callback function importing the new widget files and registering them with the widget manager.
