# Quill Focus

This package is a [Quill.js](https://quillljs.com/) module that add focus mode.

## Quickstart

### NPM Mode

Just install it as usual with npm:

```bash
> npm i quill-focus
```

And then import it in your code, something like this:

```html
<link href="/node_modules/quill-focus/src/focus.css" rel="stylesheet">
<script>
// Quill first!
var Quill = require('quill');
// Quill-Focus next
var Focus = require('quill-focus');
Quill.register('modules/focus', Focus)
var quill = new Quill('#editor', {
    theme: 'snow',
    modules: {
    focus: {
            focusClass: 'focused-blot' // Defaults to .focused-blot.
        }
    }
});
</script>
```

Done!


### Normal HTML

To install the module, set up an instance of Quill, add a script tag to the focus.js file and register it as a Quill module.
Don't forget to link default focus stylesheet. See example.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Quill-Focus Example</title>

    <link href="https://unpkg.com/quill@latest/dist/quill.snow.css" rel="stylesheet">
    <!-- Link Base Stylesheet -->
    <link href="https://rawgit.com/amka/quill-focus/master/src/focus.css" rel="stylesheet">
</head>

<body>
    <div class="container">
        <div id="editor"></div>

        <script src="https://unpkg.com/quill@latest/dist/quill.js"></script>

        <!-- Link Focus module -->
        <script src="https://rawgit.com/amka/quill-focus/master/src/focus.js"></script>
        <script>
            // Don't forget to register module
            Quill.register('modules/focus', Focus)

            var quill = new Quill('#editor', {
                theme: 'snow',
                modules: {
                    // Activate Focus module
                    focus: {
                        focusClass: 'focused-blot' // Defaults to .focused-blot.
                    }
                }
            });
        </script>
    </div>
</body>

</html>
```

---
Thanks!
