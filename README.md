# [Hyperapp](https://hyperapp.js.org)

[![Travis CI](https://img.shields.io/travis/hyperapp/hyperapp/master.svg)](https://travis-ci.org/hyperapp/hyperapp) [![Codecov](https://img.shields.io/codecov/c/github/hyperapp/hyperapp/master.svg)](https://codecov.io/gh/hyperapp/hyperapp) [![npm](https://img.shields.io/npm/v/hyperapp.svg)](https://www.npmjs.org/package/hyperapp) [![Slack](https://hyperappjs.herokuapp.com/badge.svg)](https://hyperappjs.herokuapp.com "Join us")

Hyperapp is a JavaScript library for building web applications. And this is my first demo using it.

## Examples

Here is the first example to get you started. You can [try it online](https://codepen.io/hyperapp/pen/zNxZLP) too.

```jsx
import { h, app } from "hyperapp"

const state = {
  count: 0
}

const actions = {
  down: () => state => ({ count: state.count - 1 }),
  up: () => state => ({ count: state.count + 1 })
}

const view = (state, actions) => (
  <main>
    <h1>{state.count}</h1>
    <button onclick={actions.down}>-</button>
    <button onclick={actions.up}>+</button>
  </main>
)

const main = app(state, actions, view, document.body)
```

## Installation

Install with npm or Yarn.

<pre>
npm i <a href="https://www.npmjs.com/package/hyperapp">hyperapp</a>
</pre>

Then with a module bundler like [Rollup](https://github.com/rollup/rollup) or [Webpack](https://github.com/webpack/webpack), use as you would anything else.

```jsx
import { h, app } from "hyperapp"
```

If you prefer not to use a build system, you can load Hyperapp from a [CDN](https://unpkg.com/hyperapp) and it will be globally available through the `window.hyperapp` object.

```html
<!doctype html>
<html>
<body>
  <script src="https://unpkg.com/hyperapp"></script>
  <script>

  const { h, app } = hyperapp

  </script>
</body>
</html>
```

We support all ES5-compliant browsers, including Internet Explorer 10 and above.

## Community

* [Slack](https://hyperappjs.herokuapp.com)
* [/r/Hyperapp](https://www.reddit.com/r/hyperapp)
* [Twitter](https://twitter.com/hyperappjs)
