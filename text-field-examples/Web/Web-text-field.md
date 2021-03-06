<!--docs:
title: "Text field"
layout: detail
section: components
excerpt: "MDC Web Text field"
ide_version: "<cIDE name> <compatible IDE version and build number>"
material_package_version: "<compatible Material platform package version number>"
iconId:
path: /
api_doc_root:
-->

_**Instructions**_
* [Using text field](#using-text-field)
    * Add a link under [Using text field](#using-text-field) to your getting started page if you have one
    * Insert [installation](#installation) and [theming](#theming) as appropriate for your platform
    * Insert any additional instructions that apply to your platform with a separte level 3 header
    * If you have no getting started links or instructions, delete the [Using text field](#using-text-field) sections
* [Filled text](#filled-text) ane [Outlined-text](#outlined-text) sections
    * Add links to your platform 

# Text field

[Text fields](https://material.io/components/text-fields) let users enter and edit text.

For more information, go the the [`mdc-text-field` API](#mdc-text-field-api) documentation.

The text field class consists of the following types:

* [Filled text](#filled-text)
* [Outlined text](#outlined-text)


<img src="assets/text-field-generic.png" alt="Text field examples of both filled and outlined types, and each type showing both inactive and focused states. The filled text fields show a gray background and a darker gray activation indicator that is purple when focused. The outlined text fields show a clear background and an outline that is purple when focused">

## Using text fields

Text fields allow users to enter text into a UI. They typically appear in forms and dialogs.

### Install the Material text field component

Install the `textfield` component before including it in you source:

```bash
npm install @material/textfield
```


### Import JavaScript effects
You can optinally add a JavaScript [line ripple](https://material.io/components/web/catalog/input-controls/line-ripple/) or [floating label](https://material.io/develop/web/components/input-controls/floating-label/) effect to your text fields by importing and then instantiating `MCDRipple` in your `*.js` file. See the page on importing the [JavaScript component](https://github.com/material-components/material-components-web/blob/master/docs/importing-js.md) for more information on importing JavaScript.

To bundle your `*.js` file, go to the [quickstart page](https://github.com/material-components/material-components-web/blob/master/docs/getting-started.md#quick-start-cdn).


```js
import {MDCTextField} from '@material/textfield';

<!-- The following line applies to the `mdc-text-field` class-->
const textField = new MDCTextField(document.querySelector('.mdc-text-field'));

```


### Sass mixins

Before using Sass mixins for your project you will need to do the following:

* Add the Sass package to your `*.json file` under `devDependencies`:
```json
"devDependencies": {
  "sass": "^1.14.3"
}
````

* Add a `.sassrc.js` file to your project directory:
```js

const path = require("path");

const CWD = process.cwd();

module.exports = {
  includePaths: [path.resolve(CWD, "node_modules"), path.resolve(CWD, "src")]
};
```

* In your `*.scss` file for your application, create an instance of your text field with the Sass mixins settings of your choice. For example, if you have a text field:

```css
.text-field-instance {
  @include mdc-text-field-label-color(orange);
  @include mdc-text-field-label-caret-color(green);
  ...
}
```

<img src="assets/web-sass-mixins-example.png" alt="Example text field instance rendered for an orange label and a green cursor caret">


#### Sass mixins for `mdc-text-field`

Use Sass mixins when you want to customize the look and feel of your text fields. Go to [sass-lang.com](https://sass-lang.com/install) for installation instructions.

Text fields support [Material Theming](https://material.io/components/text-fields/#theming) and can be customized in terms of color, typography, and shape.

Before using Sass mixins for your project you will need to do the following:

* Add the Sass package to your `*.json file` under `devDependencies`:
```json
"devDependencies": {
  "sass": "^1.24.3"
}
```

* Add a `.sassrc.js` file to your project root directory:

```js
const path = require("path");

const CWD = process.cwd();

module.exports = {
  includePaths: [path.resolve(CWD, "node_modules"), path.resolve(CWD, "src")]
};
```


Import base styles of button into your `*.scss` stylesheet using :

**NOTE are there theming instructions for text fields? Include them in the collapsible section**


### Making text fields accessible

The web platform's text field component APIs supports both label text and helper text for accessibility. 

For more guidance on writing labels, go to [our page on how to write a good accessibility label](https://material.io/design/usability/accessibility.html#writing).


## Filled text

[Filled text fields](https://material.io/components/text-fields/#filled-text-field) have more visual emphasis than outlined text fields, making them stand out when surrounded by other content and components.

### Filled text example

Source code API:

* `TextInputLayout` 
  * [Class definition]()
  * [GitHub source](https://github.com/material-components/)

The following examples shows a filled text field.


_**Copy the image to your platform's assets folder. Use a screenshot of your render.**_


<img src="assets/.png" alt="filled text field for Android">

```
* The label text should read "Label text"
* The input text should read "Input text"
* The helper text should read "Helper text"
* The text field should have a character counter of up to 20 characters
* The text field should have a "favorite" leading icon
```

### Anatomy and key properties

![filled text field anatomy](assets/textfields_filled_anatomy.png)

1. Container
1. Leading icon (optional)
1. Label text
1. Input text
1. Trailing icon (optional)
1. Activation indicator
1. Helper text (optional)

<b>Container</b>

| Design Attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Color** | |`mdc-text-field-fill-color($color)` | 
| **Stroke color** | |`mdc-text-field-bottom-line-color($color) | 
| **Stroke color(hover)** | |`mdc-text-field-hover-bottom-line-color($color)`  |
| **Shape** | |`mdc-text-field-shape-radius($radius, $rtl-reflexive)`| 
| **Elevation** | | | 
| **Ripple color** | |`mdc-text-field-line-ripple-color($color)` | 

<<b>Leading icon (optional) </b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Icon** | | |
| **Color** | | | 
| **Size** | | | 
| **Gravity** | | | 
| **Padding** | | |


</details>


<b>Label text</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Label text** |  | | 
| **Typography** | | | 
| **Color** | |`mdc-text-field-label-color($color)` | 

<b>Input text</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Label text** |  |`mdc-text-field-ink-color($color)`  |
| **Typography** | | |
| **Color** | |`mdc-text-field-ink-color($color)` |
| **Cursor color** | | `mdc-text-field-caret-color($color)` |

<b>Trailing icon (optional) </b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Icon** | | | 
| **Color** | | |
| **Size** | | |
| **Gravity** | | |
| **Padding** | | | 

<b>Activation indicator</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- | 
| **Stroke color** | | |
| **Stroke width** | | |
| **Ripple color** | | |
| **Stroke color(hover)** | |`mdc-text-field-hover-bottom-line-color($color)`  |

<b>Helper text (optional)</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Label text** |  | |
| **Typography** | | |
| **Color** | | | 

## Outlined text

[Outlined text fields](https://material.io/components/text-fields/#outlined-text-field) have less visual emphasis than filled text fields. When they appear in places like forms, where many text fields are placed together, their reduced emphasis helps simplify the layout.

### Outlined text example

Source code API:

* `TextInputLayout` 
  * [Class definition]()
  * [GitHub source]()

The following examples shows an outlined text field.

_**Copy the image to your platform's assets folder. Use a screenshot of your render.**_
<img src="assets/.png" alt="outlined text field for Android.">

```
* The label text should read "Label text"
* The input text should read "Input text"
* The error message text should read "Error message" and display the error message
* The text field should have a trailing error icon
```
### Anatomy and key properties

![Outlined text field anatomy](assets/textfields_outlined_anatomy.png)

1. Container
1. Leading icon (optional)
1. Label text
1. Input text
1. Trailing icon (optional)
1. Activation indicator
1. Helper text (optional)

<b>Container</b>

| Design Attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Color** | |`mdc-text-field-fill-color($color)` | 
| **Stroke color** | |`mdc-text-field-outline-color($color) | 
| **Stroke color(hover)** | |`mdc-text-field-hover-outline-color($color)`  |
| **Shape** | |`mdc-text-field-shape-radius($radius, $rtl-reflexive)`| 
| **Elevation** | | | 
| **Ripple color** | |`mdc-text-field-line-ripple-color($color)` | 

<b>Leading icon (optional)</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Icon** | | |
| **Color** | | | 
| **Size** | | | 
| **Gravity** | | | 
| **Padding** | | |

<b>Label text</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Label text** |  | | 
| **Typography** | | | 
| **Color** | |`mdc-text-field-label-color($color)` | 

<b>Input text</b> 

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Label text** |  |`mdc-text-field-ink-color($color)`  |
| **Typography** | | |
| **Color** | |`mdc-text-field-ink-color($color)` |
| **Cursor color** | | `mdc-text-field-caret-color($color)` |

<b>Trailing icon (optional)</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- | 
| **Color** | | | 
| **Stroke color** | | | 
| **Stroke width** | | |
| **Shape** | | | 
| **Elevation** | | | 
| **Ripple color** | | | 

<b>Activation indicator</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- |
| **Stroke color** | |`mdc-text-field-focused-outline-color($color)`  |
| **Stroke width** | | |
| **Ripple color** | | |

<b>Helper text (optional)</b>

|  Design attribute | Theme value | Equivalent Sass mixin attribute |
| --- | --- | --- | 
| **Label text** |  | | 
| **Typography** | | | 
| **Color** | | | 


## Theming text fields

Text fields support [Material Theming](https://material.io/components/text-fields/#theming) and can be customized in terms of color, typography and shape.

### Text field theming example

API and source code:

* `\<Component platform API name\>`
    * [Class description](https://)
    * [GitHub source](https://github.com/material-components/)
    
The following example shows filled and outlined text fields with Material Theming.

!["Two text fields, one filled, one outlined, with green/black color theming and cut corners."](assets/button-theming.svg)

_Use the [Shrine theme](https://material.io/design/material-studies/shrine.html) for this example_


```
* Include one filled text field with the following:
    * The label text should read "Label text"
    * The input text should read "Input text"
    * The helper text should read "Helper text"
    * The text field should have a character counter of up to 20 characters
    * The text field should have a "favorite" leading icon
    * The container should have cut corners instead of rounded
* Include one outlined text field with the following:
    * The label text should read "Label text"
    * The input text should read "Input text"
    * The error message text should read "Error message" and display the error message
    * The text field should have a trailing error icon
    * The container should have cut corners instead of rounded
```

## `mdc-text-field` API

### CSS Classes

CSS Class | Description
--- | ---
`mdc-text-field` | Mandatory.
`mdc-text-field--outlined` | Styles the text field as an outlined text field.
`mdc-text-field--fullwidth` | Styles the text field as a full width text field.
`mdc-text-field--textarea` | Indicates the text field is a `<textarea>`.
`mdc-text-field--disabled` | Styles the text field as a disabled text field.
`mdc-text-field--dense` | Styles the text field as a dense text field.\*
`mdc-text-field--with-leading-icon` | Styles the text field as a text field with a leading icon.
`mdc-text-field--with-trailing-icon` | Styles the text field as a text field with a trailing icon.
`mdc-text-field--focused` | Styles the text field as a text field in focus.
`mdc-text-field--no-label` | Styles the text field that has no label.
`mdc-text-field--end-aligned` | Styles the text field with an end-aligned input.
`mdc-text-field-helper-line` | Styles the container of helper text and character counter elements.

#### Deprecation Notice

\*The `--dense` variant of the text field will be removed in an upcoming release.
See [github issue](https://github.com/material-components/material-components-web/issues/4142) for details.

### Sass Mixins

To customize the colors of any part of the text-field, use the following mixins. We recommend you apply
these mixins within CSS selectors like `.foo-text-field:not(.mdc-text-field--focused)` to select your unfocused text fields,
and `.foo-text-field.mdc-text-field--focused` to select your focused text-fields. To change the invalid state of your text fields,
apply these mixins with CSS selectors such as `.foo-text-field.mdc-text-field--invalid`.

> _NOTE_: the `mdc-line-ripple-color` mixin should be applied from the not focused class `foo-text-field:not(.mdc-text-field--focused)`).

#### Mixins for all Text Fields

Mixin | Description
--- | ---
`mdc-text-field-ink-color($color)` | Customizes the color of the text entered into an enabled text field.
`mdc-text-field-placeholder-color($color)` | Customizes the color of the placeholder in an enabled text field.
`mdc-text-field-disabled-ink-color($color)` | Customizes the color of the entered text in a disabled text field.
`mdc-text-field-disabled-placeholder-color($color)` | Customizes the color of the placeholder in a disabled text field.
`mdc-text-field-label-color($color)` | Customizes the text color of the label in an enabled text field.
`mdc-text-field-disabled-label-color($color)` | Customizes the text color of the label in a disabled text field.
`mdc-text-field-caret-color($color)` | Customizes the color of the cursor caret of the text field.

#### Mixins for Filled Text Field and Textarea

Mixin | Description
--- | ---
`mdc-text-field-fill-color($color)` | Customizes the background color of the text field or textarea when enabled.
`mdc-text-field-disabled-fill-color($color)` | Customizes the background color of the text field or textarea when disabled.

#### Mixins for Filled Text Field Only

Mixin | Description
--- | ---
`mdc-text-field-shape-radius($radius, $rtl-reflexive)` | Sets rounded shape to boxed text field variant with given radius size. Set `$rtl-reflexive` to true to flip radius values in RTL context, defaults to false.
`mdc-text-field-bottom-line-color($color)` | Customizes the text field bottom line color.
`mdc-text-field-hover-bottom-line-color($color)` | Customizes the hover text field bottom line color.
`mdc-text-field-disabled-bottom-line-color($color)` | Customizes the disabled text field bottom line color.
`mdc-text-field-line-ripple-color($color)` | Customizes the color of the default line ripple of the text field.
`mdc-text-field-density($density-scale)` | Sets density scale for default text field variant. Supported density scale values `-4`, `-3`, `-2`, `-1`, `0`.
`mdc-text-field-height($height)` | Sets height of default text field variant.

#### Mixins for Outlined Text Field and Textarea

Mixin | Description
--- | ---
`mdc-text-field-focused-outline-color($color)` | Customizes the outline border color when the text field or textarea is focused.
`mdc-text-field-hover-outline-color($color)` | Customizes the outline border color when the text field or textarea is hovered.
`mdc-text-field-disabled-outline-color($color)` | Customizes the outline border color when the text field or textarea is disabled.
`mdc-text-field-outline-color($color)` | Customizes the border color of the outlined text field or textarea.

#### Mixins for Outlined Text Field Only

Mixin | Description
--- | ---
`mdc-text-field-outline-shape-radius($radius, $rtl-reflexive)` | Sets rounded shape to outlined text field variant with given radius size. Set `$rtl-reflexive` to true to flip radius values in RTL context, defaults to false.
`mdc-text-field-outlined-density($density-scale)` | Sets density scale for outlined text field (Excluding outlined text field with leading icon). Supported density scale values `-4`, `-3`, `-2`, `-1`, `0`.
`mdc-text-field-outlined-height($height)` | Sets height of outlined text field variant (Excluding outlined text field with leading icon).
`mdc-text-field-outlined-with-leading-icon-density($density-scale)` | Sets density scale for outlined text field with leading icon. Supported density scale values `-4`, `-3`, `-2`, `-1`, `0`.
`mdc-text-field-outlined-with-leading-icon-height($height)` | Sets height of outlined text field with leading icon variant.

#### Mixins for Textarea Only

Mixin | Description
--- | ---
`mdc-text-field-textarea-shape-radius($radius, $rtl-reflexive)` | Sets rounded shape to text area variant with given radius size. Set `$rtl-reflexive` to true to flip radius values in RTL context, defaults to false.

## `MDCTextField` Properties and Methods

Property | Value Type | Description
--- | --- | ---
`value` | `string` | Proxies to the foundation's `getValue`/`setValue` methods.
`disabled` | `boolean` | Proxies to the foundation's `isDisabled`/`setDisabled` methods.
`useNativeValidation` | `boolean` (write-only) | Proxies to the foundation's `setUseNativeValidation` method.
`valid` | `boolean` | Proxies to the foundation's `isValid`/`setValid` methods.
`helperTextContent` | `string` (write-only)| Proxies to the foundation's `setHelperTextContent` method when set.
`ripple` | `MDCRipple` (write-only) | The `MDCRipple` instance for the root element that `MDCTextField` initializes; this only applies to the default Text Field, and is `null` for other variants.
`leadingIconAriaLabel` | `string` (write-only) | Proxies to the foundation's `setLeadingIconAriaLabel` method.
`trailingIconAriaLabel` | `string` (write-only) | Proxies to the foundation's `setTrailingIconAriaLabel` method.
`leadingIconContent` | `string` (write-only) | Proxies to the foundation's `setLeadingIconContent` method.
`trailingIconContent` | `string` (write-only) | Proxies to the foundation's `setTrailingIconContent` method.

In addition to the above, the following properties proxy to the `input` element's properties of the same name:

* `required`
* `pattern`
* `minLength`
* `maxLength`
* `min`
* `max`
* `step`

Method Signature | Description
--- | ---
`focus() => void` | Focuses the `input` or `textarea` element.
`layout() => void` | Adjusts the dimensions and positions for all sub-elements.

## Usage Within Frameworks

If you are using a JavaScript framework, such as React or Angular, you can create a Text Field for your framework. Depending on your needs, you can use the _Simple Approach: Wrapping MDC Web Vanilla Components_, or the _Advanced Approach: Using Foundations and Adapters_. Please follow the instructions [here](../../docs/integrating-into-frameworks.md).

### `MDCTextFieldAdapter`

Method Signature | Description
--- | ---
`addClass(className: string) => void` | Adds a class to the root element.
`removeClass(className: string) => void` | Removes a class from the root element.
`hasClass(className: string) => boolean` | Returns true if the root element contains the given class name.
`registerTextFieldInteractionHandler(evtType: string, handler: EventListener) => void` | Registers an event handler on the root element for a given event.
`deregisterTextFieldInteractionHandler(evtType: string, handler: EventListener) => void` | Deregisters an event handler on the root element for a given event.
`registerInputInteractionHandler(evtType: string, handler: EventListener) => void` | Registers an event listener on the native input element for a given event.
`deregisterInputInteractionHandler(evtType: string, handler: EventListener) => void` | Deregisters an event listener on the native input element for a given event.
`registerValidationAttributeChangeHandler(handler: (attributeNames: string[]) => void) => MutationObserver` | Registers a validation attribute change listener on the input element. Handler accepts list of attribute changes.
`deregisterValidationAttributeChangeHandler(!MutationObserver) => void` | Disconnects a validation attribute observer on the input element.
`getNativeInput() => NativeInputType \| null` | Returns an object representing the native text input element, with a similar API shape. See [types.ts](types.ts).
`isFocused() => boolean` | Returns whether the input is focused.
`shakeLabel(shouldShake: boolean) => void` | Shakes the label to indicate an invalid input value.
`floatLabel(shouldFloat: boolean) => void` | Floats the label.
`hasLabel() => boolean` | Determines whether the text field has a label element.
`getLabelWidth() => number` | Returns the width of the label element in px.
`activateLineRipple() => void` | Activates the text field's line ripple sub-element.
`deactivateLineRipple() => void` | Deactivate the text field's line ripple sub-element.
`setLineRippleTransformOrigin(normalizedX: number) => void` | Sets the CSS `transform-origin` property to the given value on the text field's line ripple sub-element (if present).
`hasOutline() => boolean` | Determines whether the text field has an outline sub-element.
`notchOutline(labelWidth: number) => void` | Sets the width of the text field's notched outline sub-element.
`closeOutline() => void` | Closes the text field's notched outline sub-element.

#### `MDCTextFieldAdapter.getNativeInput()`

Returns an object representing the native text input element, with a similar API shape. We _never_ alter the value within our code, however we _do_ update the disabled property, so if you choose to duck-type the return value for this method in your implementation it's important to keep this in mind. Also note that this method can return null, which the foundation will handle gracefully.

#### `MDCTextFieldAdapter.getIdleOutlineStyleValue(propertyName: string)`

Returns the idle outline element's computed style value of the given css property `propertyName`. The vanilla implementation achieves this via `getComputedStyle(...).getPropertyValue(propertyName)`.

### `MDCTextFieldFoundation`

Property | Value Type | Description
--- | --- | ---
`shouldFloat` | `boolean` (read-only) | Determines whether the label should float.
`shouldShake` | `boolean` (read-only) | Determines whether the label should shake.

Method Signature | Description
--- | ---
`getValue() => string` | Returns the input's value.
`setValue(value: string)` | Sets the input's value.
`setUseNativeValidation(useNativeValidation: boolean)` | Sets whether to check native HTML validity state (`true`, default) or custom validity state when updating styles (`false`).
`setValid(isValid: boolean)` | Sets custom validity and updates styles accordingly. Note that native validation will still be honored subsequently unless `setUseNativeValidation(false)` is also called.
`isValid() => boolean` | Returns the component's current validity state (either native or custom, depending on how `setUseNativeValidation()` was configured).
`isDisabled() => boolean` | Returns whether or not the input is disabled.
`setDisabled(disabled: boolean) => void` | Updates the input's disabled state.
`handleTextFieldInteraction(evt: Event) => void` | Handles click and keydown events originating from inside the Text Field component.
`handleInput() => void` | Handles text input and textarea input event.
`handleValidationAttributeChange(attributesList: !Array<string>) => void` | Handles validation attribute changes.
`activateFocus() => void` | Activates the focus state of the Text Field. Normally called in response to the input focus event.
`deactivateFocus() => void` | Deactivates the focus state of the Text Field. Normally called in response to the input blur event.
`setHelperTextContent(content: string) => void` | Sets the content of the helper text.
`setLeadingIconAriaLabel(label: string) => void` | Sets the aria label of the leading icon.
`setLeadingIconContent(content: string) => void` | Sets the text content of the leading icon.
`setTrailingIconAriaLabel(label: string) => void` | Sets the aria label of the trailing icon.
`setTrailingIconContent(content: string) => void` | Sets the text content of the trailing icon.
`notchOutline(openNotch: boolean) => void` | Opens/closes the notched outline.
`setTransformOrigin(evt: TouchEvent \| MouseEvent) => void` | Sets the line ripple's transform origin, so that the line ripple activate animation will animate out from the user's click location.
`autoCompleteFocus() => void` | Activates the Text Field's focus state in cases when the input value is changed programmatically (i.e., without user action).

`MDCTextFieldFoundation` supports multiple optional sub-elements: helper text and icon. The foundations of these sub-elements must be passed in as constructor arguments to `MDCTextFieldFoundation`.

