
# ITCSS
Inverted Triangle CSS
CSS / Sass architectural principles for large scale CSS projects

- http://thomasbyttebier.be/blog/less-css-mess?utm_source=CSS-Weekly&utm_campaign=Issue-180&utm_medium=email
- https://speakerdeck.com/dafed/managing-css-projects-with-itcss
- https://www.youtube.com/watch?v=1OKZOV-iLj4&hd=1
- https://twitter.com/itcss_io

## Layers:
Starting generic and getting more specific.


### Settings
Global Variables, Config Switches
- Globally available settings
- Config Switches
- Brand colours etc

##### File names:
```_settings.[FILE NAME].scss``` e.g. ```_settings.colours.scss```

### Tools
Default mixins and functions
- Globally available tools
- Public mixins
- Helper functions

### Generic
Ground-zero styles (Normalize.css, resets, box-sizing)
- Ground-zero styles
- Low specificity & far-reaching
- Resets, Normalize.css etc

```css
* {
  -webkit-box-sizing:border-box;
     -moz-box-sizing:border-box;
          box-sizing:border-box;
}
```

##### File names:
```_generic.[FILE NAME].scss``` e.g. ```_generic.normalize.scss```

### Base
Unclassed HTML elements (type selectors)
- Unclassed HTML elements
- H1-H6, base links, lists etc
- Last layer we see type selectors (e.g. a {}, blockquote {})

##### File names:
```_base.[FILE NAME].scss``` e.g. ```_base.typography.scss```


### Objects
Cosmetic-free design patterns
- OOCSS
- Design patterns
- No cosmetics
- Begin using classes exclusively
- Agnostically named (e.g. ui-list {})

##### File names:
```_object.[FILE NAME].scss``` e.g. ```_object.media.scss```


### Components
Designed components, chunks of UI
- Designed pieces of UI
- Still only using classes
- More explicitly named (e.g. .products-list {})

##### File names:
```_component.[FILE NAME].scss``` e.g. ```_component.site-header.scss```


### Trumps / Wins
Helpers and overrides
- Overrides, helpers, utilities
- Only affect one piece of the DOM at a time
- Usually carry !important

Class names prefixed with 'u-' e.g.```u-clearfix```


### Optional layers
For example:
- Themes
- Tests

These should be inserted at the right point in the hierarchy (most likely between Components and Trumps/Wins)
