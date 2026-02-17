# [MathQuill](http://mathquill.com)

## Roebling Developers

### Overview

This is a fork of the **MathQuill** project. It adds support for some non-standard LaTeX behavior, such as objects (e.g `MyVariable`) and object properties (e.g `Flow.rate.x`). Identifiers are assigned new `mq-identifier ...` class names so that they can be syntax highlighted.

To rebuild the code after making a change, run `make all` in the root directory. You can then run an example in your browser by opening e.g `examples/synonym.html`. You need to re-run `make all` after any change in the library.

Before exporting the build to `synonym-react-mathquill`, make sure to run `make basic` also!

### Changes
- Added the `_` character in `parser.util.ts`
- Got rid of the special `mq-f` class
- Commented out the `SubscriptCommand`
- Added the `parseSemanticTypes` function in `publicapi.ts`
- Extended unit brace detection to support `VanillaSymbol` and `NonSymbolaSymbol` nodes (e.g `%`, `$`) inside `\left\{...\right\}`, not just `Letter` and `Digit`

---

## Original README

by [Han](http://github.com/laughinghan), [Jeanine](http://github.com/jneen), and [Mary](http://github.com/stufflebear) (<maintainers@mathquill.com>) [<img alt="slackin.mathquill.com" src="http://slackin.mathquill.com/badge.svg" align="top">](http://slackin.mathquill.com)

MathQuill is a web formula editor designed to make typing math easy and beautiful.

[<img alt="homepage demo" src="https://cloud.githubusercontent.com/assets/225809/15163580/1bc048c4-16be-11e6-98a6-de467d00cff1.gif" width="260">](http://mathquill.com)

The MathQuill project is supported by its [partners](http://mathquill.com/partners.html). We hold ourselves to a compassionate [Code of Conduct](http://docs.mathquill.com/en/latest/Code_of_Conduct/).

MathQuill is resuming active development and we're committed to getting things running smoothly. Find a dusty corner? [Let us know in Slack.](http://slackin.mathquill.com) (Prefer IRC? We're `#mathquill` on Freenode.)

## Getting Started

MathQuill has a simple interface. This brief example creates a MathQuill element and renders, then reads a given input:

```javascript
var htmlElement = document.getElementById('some_id');
var config = {
  handlers: { edit: function(){ ... } },
  restrictMismatchedBrackets: true
};
var mathField = MQ.MathField(htmlElement, config);

mathField.latex('2^{\\frac{3}{2}}'); // Renders the given LaTeX in the MathQuill field
mathField.latex(); // => '2^{\\frac{3}{2}}'
```

Check out our [Getting Started Guide](http://docs.mathquill.com/en/latest/Getting_Started/) for setup instructions and basic MathQuill usage.

## Docs

Most documentation for MathQuill is located on [ReadTheDocs](http://docs.mathquill.com/en/latest/).

Some older documentation still exists on the [Wiki](https://github.com/mathquill/mathquill/wiki).

## Open-Source License

The Source Code Form of MathQuill is subject to the terms of the Mozilla Public
License, v. 2.0: [http://mozilla.org/MPL/2.0/](http://mozilla.org/MPL/2.0/)

The quick-and-dirty is you can do whatever if modifications to MathQuill are in
public GitHub forks. (Other ways to publicize modifications are also fine, as
are private use modifications. See also: [MPL 2.0 FAQ](https://www.mozilla.org/en-US/MPL/2.0/FAQ/))
