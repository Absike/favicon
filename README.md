# favicon.js `1.0.0`

Finds a website’s favicon URL, if any. Requires a context, like a browser extension, that allows cross-origin requests.

## Example

```html
<script type="text/javascript" src="favicon.js"></script>
<script type="text/javascript">
  var favicon = new Favicon();

  favicon.get('https://disconnect.me/', function(url) {
    jQuery('img').attr('src', url); // favicon.js automagically loads jQuery.
  });
</script>
<img width="16" height="16" src="default.png" alt="A favicon.">
```

## Constructor

### Favicon([{string} alternate=""])

A class for finding a website’s favicon URL, if any.

#### Parameter

`alternate` A default favicon URL, absolute or relative.

## Methods

### {string} getAlternate()

Fetches the default favicon URL.

#### Return value

An absolute or relative URL.

### {Favicon} setAlternate({string} alternate)

Mungs the default favicon URL.

#### Parameter

`alternate` An absolute or relative URL.

#### Return value

The favicon object.

### {Favicon|string} get({string} url[, {function(string)} callback])

Finds a favicon URL.

#### Parameters

`url` A website’s hostname or absolute URL.
`callback` A continuation, to execute when the method completes.

#### Return value

The favicon object, if a continuation is given, or a URL, if not.

## Author

[Brian Kennish](https://github.com/byoogle)

## License

Copyright 2012 Disconnect, Inc.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the [GNU General Public License](https://www.gnu.org/licenses/gpl.html) for more details.

## See also

[jQuery](https://github.com/jquery/jquery)