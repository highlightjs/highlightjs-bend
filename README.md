# Bend - a language grammar for [bend programming language](https://higherorderco.com/)


Bend is a high-level language for native multi-threading created by [The higher order company](https://higherorderco.com/).

## Usage

Simply include the Highlight.js library in your webpage or Node app, then load this module.

### Static website or simple usage

Simply load the module after loading Highlight.js. You'll use the minified version found in the `dist` directory. This module is just a CDN build of the language, so it will register itself as the Javascript is loaded.

```html
<script type="text/javascript" src="/path/to/highlight.min.js"></script>
<script type="text/javascript" charset="UTF-8"
  src="/path/to/highlightjs-bend/dist/bend.min.js"></script>
<script type="text/javascript">
  hljs.highlightAll();
</script>
```

### Using directly from the UNPKG CDN

```html
<script type="text/javascript"
  src="https://unpkg.com/highlightjs-bend/dist/bend.min.js"></script>
```

- More info: <https://unpkg.com>

### With Node or another build system

If you're using Node / Webpack / Rollup / Browserify, etc, simply require the language module, then register it with Highlight.js.

```javascript
var hljs = require('highlightjs');
var hljsBend = require('highlightjs-bend');

hljs.registerLanguage("bend", hljsBend);
hljs.highlightAll();
```

### React

You need to import both Highlight.js and third-party language like Bend:

```js
import React, {Component} from 'react'
import 'highlight.js/scss/darcula.scss' # your favourite theme
import bend from './bend'
import hljs from 'highlight.js'
hljs.registerLanguage('bend', bend);

class Highlighter extends Component
{
  constructor(props)
  {
    super(props);
    hljs.highlightAll();
  }

  render()
  {
    let {children} = this.props;
    return
    {
      <pre ref={(node) => this.node = node}>
        <code className="bend">
          {children}
        </code>
      </pre>
    }
  }
}

export default Highlighter;
```

## License

Highlight.js is released under the MIT 1.0 License. See [LICENSE][1] file
for details.

### Author

Rohan Vashisht <learncodingly@gmail.com> [https://github.com/rohanvashisht1234](https://github.com/rohanvashisht1234)

### Maintainer

Rohan Vashisht <learncodingly@gmail.com> [https://github.com/rohanvashisht1234](https://github.com/rohanvashisht1234)

## Links

- The official site for the Highlight.js library is <https://highlightjs.org/>.
- The Highlight.js GitHub project: <https://github.com/highlightjs/highlight.js>

[1]: https://github.com/highlightjs/highlightjs-bend/blob/master/LICENSE
