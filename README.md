# jquery-menubar
Completely accessible and 508 compliant menubar extension for jQuery UI.

Coded up by Marvin Herbold

This jQuery UI menubar code just re-uses the current built-in jquery ui menu widget and tweaks it a little bit to add full menubar support - the tweaks done are as follows:

* Split position option into downPosition and rightPosition options
* Split submenu icon option into submenuDown and submenuRight icon options
* Split role option into role (default=menubar) and submenuRole (default=menu) options
* Switch around right/left/up/down keyboard mapping for top level menu items
* Only "-" will be converted to dividers - not spaces

That's it! All jQuery UI menu options and callbacks are supported.

## Known Issues
The native jQuery menu widget has a few issues with the coloring of icons and anchors. This project includes a fix for the coloring of anchors, but I am still working on a fix for the coloring of icons in submenus.

## Usage
$( selector ).menubar();

## Options
The options are nearly identical to the jQuery menu widget and in fact many get passed directly to the jQuery menu widget.

```
options: {
  icons: {
    submenuDown: "ui-icon-carat-1-s",
    submenuRight: "ui-icon-carat-1-e"
  },
  items: "> *",
  menus: "ul",
  downPosition: {
    my: "left top",
    at: "left bottom"
  },
  rightPosition: {
    my: "left top",
    at: "right top"
  },
  role: "menubar",
  submenuRole: "menu",

  // callbacks
  blur: null,
  focus: null,
  select: null
}
```

## Proof It Works
https://jsfiddle.net/mherbold/n8z7wghu/
