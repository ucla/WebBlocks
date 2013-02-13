# Entity/Nav/Breadcrumb

## Definition

Breadcrumb navigation is used to display the User's current location within a website. For example, if a User is
visiting the "Types" section of the "Apples" section within the "Fruit" section of a website, they might see the 
following breadcrumb navigation:

``
Fruit > Apples > Types
``

In this example, "Fruit" and "Apples" would be links to those respective sections of the website. Breadcrumb navigation
should not be used as the primary navigation of a website.

## Usages

* Display the ancestor sections leading to the User's current section on the website

## Features

### Ordered vs Unordered

An `ol` element is considered more semantic over a `ul` for breadcrumb navigation due to the fact that there is an
ordering to the items within the breadcrumb (a hierarchical ordering).

### Links vs Plain Text

Although using links is recommended for optimum usability, the breadcrumb trail does not necessarily need to contain
links. Plain text can be used instead.

### "Active" Breadcrumb Item

To denote the "active" or "current" item in the breadcrumb trail, add the "active" CSS class to the `li` element
containing the breadcrumb item.

### Dividers

A breadcrumb can be styled using CSS, of course, but you can also use a simpler text-based divider glyph between
each of the items within your breadcrumb trail by adding a `span` element with CSS class "divider" containing the
divider glyph (a "/" or ":", for example).

### Examples

```html
<ol class="breadcrumb">
    <li>
        <a href="#1">Item 1</a>
        <span class="divider">></span>
    </li>
    <li>
        <a href="#2">Item 2</a>
        <span class="divider">></span>
    </li>
    <li>
        <a href="#3">Item 3</a>
    </li>
</ol>
```

Plain text can be used instead of links:

```html
<ol class="breadcrumb">
    <li>
        <a href="#1">Item 1</a>
        <span class="divider">/</span>
    </li>
    <li>
        Plain Text Item
        <span class="divider">/</span>
    </li>
    <li>
        <a href="#1">Item 3</a>
    </li>
</ol>
```

Designate the "active" or currently selected item by adding the "active" CSS class to the `li` element
containing the breadcrumb item:

```html
<ol class="breadcrumb">
    <li>
        <a href="#1">Item 1</a>
        <span class="divider">&raquo;</span>
    </li>
    <li>
        <a href="#2">Item 2</a>
        <span class="divider">&raquo;</span>
    </li>
    <li class="active">
        Active Item
    </li>
</ol>
```

As demonstrated in the examples above, a variety of different glyphs can be used as dividers.

## Responsive Considerations

The breadcrumb should fit the full width of its container, shrinking with the container in smaller viewport width.