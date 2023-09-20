# Group Controls

<Badge type="tip" vertical="top" text="Elementor Core" /> <Badge type="warning" vertical="top" text="Basic" />

Group controls are used to group together several regular controls and return them as a small popup in the editor. This helps improve UX by displaying a large number of controls in single line.

## Using Group Controls

The following controls are included in Elementor:

* [Typography](./../controls/classes/group-control-typography/) – Font size, font family, font weight, text transform, font style, line height, letter spacing and word spacing.
* [Text Shadow](./../controls/classes/group-control-text-shadow/) – Add a shadow effect to texts.
* [Box Shadow](./../controls/classes/group-control-box-shadow/) – Add a shadow effect to elements.
* [Border](./../controls/classes/group-control-border/) – Border type, border width and border color.
* [Background](./../controls/classes/group-control-background/) – Background color, background image, background gradient or background video.
* [Image Size](./../controls/classes/group-control-image-size/) – Select image sizes (thumbnail, medium, medium_large, large) or custom dimensions.
* [CSS Filter](./../controls/classes/group-control-css-filter/) – Apply CSS filters like blur, brighten, contrast, saturation or hue.

## Extending Group Controls

To create your own group control, you need to extend the `\Elementor\Group_Control_Base` abstract class:

```php {1}
class Elementor_Test_Control extends \Elementor\Group_Control_Base {
}
```
