# Form elements
Features, design, functionality and considerations for form elements.

## Select/textbox
Have functionality for select/textbox hybrid similar to that found on D3up.com - with [placeholder text] over [search field] over [select list].
Should be able to set number of listed items (with hardcoded minimum), and maximum number of items (for dynamically adjusting number of items listed - based on list length, capping at the set maximum).
Should have hardcoded maximum number of listed items.

## Text field
Decide on markup language to use (could be BBCode or Markdown as examples). This should apply to all text fields on site that specify support for markup.
Will there be any text fields _without_ support for this? Perhaps e-mail form for contacting site admin?

## Input

# password
When entering text in a `password` type field, we want a delay in changing the last entered character to be turned into a (dot) or (asterisk). This will most likely mean having to use a custom tag for typing the field to password.
This should include feature detection, so that the field is reverted to `type="password"` if the features we are using are not supported.

# placeholder
We want to use the HTML5 `placeholder` attribute - but feature detection should be used, and if not supported by the browser we should use jQuery to emulate the behavior. Is Modernizr able to detect this?