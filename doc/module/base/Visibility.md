# Base/Visibility

## Definition

This library provides several helper utilities related to visibility. The
classes described in this module may be applied to any element and define
visibility unless the element is already hidden by a parent element.

## Usages

The `Base/Visibility/Hide` library provides a helper that sets visibility to
none for all devices. This is useful in the context of Javascript by adding and
removing this class to change visibility. An alternative might be using the
`display:none` property such as in jQuery.

The `Base/Visibility/Responsive/Show` library provides helpers that set visibility
to none for devices with viewport dimensions that **do** meet the breakpoints
specified as `$breakpoint-small`, `$breakpoint-medium`, and `$breakpoint-large`.

The `Base/Visibility/Responsive/Show` library provides helpers that set visibility
to none for devices with viewport dimensions that **don't** meet the breakpoints
specified as `$breakpoint-small`, `$breakpoint-medium` and `$breakpoint-large`.

## Features

### Base/Visibility/Hide

* `.hide` hides the element on all devices

### Base/Visibility/No_Media_Queries

* `.hide-media-query` hides the element if the browser supports media queries.
This is an analog to the `noscript` tag.

### Base/Visibility/Responsive/Hide

* `.hide-small` hides the element on all devices smaller than 
`$breakpoint-small`
* `.hide-medium` hides the element on all devices smaller than 
`$breakpoint-medium` and at least as large as `$breakpoint-small`
* `.hide-large` hides the element on all devices smaller than
`$breakpoint-large` and at least as large as `$breakpoint-medium`
* `.hide-exlarge` hides the element on all devices at least as large as 
`$breakpoint-large`

### Base/Visibility/Responsive/Show

* `.show-small` shows the element on all devices smaller than 
`$breakpoint-small`
* `.show-medium` shows the element on all devices smaller than 
`$breakpoint-medium` and at least as large as `$breakpoint-small`
* `.show-large` shows the element on all devices smaller than
`$breakpoint-large` and at least as large as `$breakpoint-medium`
* `.show-exlarge` shows the element on all devices at least as large as 
`$breakpoint-large`

## Responsive Considerations

All visibility classes in `Base/Visibility/Responsive` relate visibility of an
element to 