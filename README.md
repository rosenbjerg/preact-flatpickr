# 📅 Preact Flatpickr

[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
[![Open Source Love](https://badges.frapsoft.com/os/mit/mit.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

> Flatpickr component for Preact ported from React-flatpickr.

### Getting Started

Install the package by running:
```
npm install --save preact-flatpickr
```

```jsx
import 'flatpickr/dist/themes/material_green.css'

import Flatpickr from 'react-flatpickr'
import { Component } from 'react'

class App extends Component {
  constructor() {
    super();

    this.state = {
      date: new Date()
    };
  }

  render() {
    const { date } = this.state;
    return (
      <Flatpickr data-enable-time
        value={date}
        onChange={date => { this.setState({date}) }} />
    )
  }
}
```
* `flatpickr options`: you can pass all `flatpickr parameters` to `props.options`
* All flatpickr [hooks][hooks] can be passed as a react prop, or to `props.options`

```jsx
<Flatpickr options={{minDate: '2017-01-01'}} />
```

### Themes
Please import themes directly from the `flatpickr` dependency. In most cases, you should just be able to `import 'flatpickr/dist/themes/theme.css'`, but in some cases npm or yarn may install `flatpickr` in `node_modules/react-flatpickr/node_modules/flatpickr`. If that happens, removing your `node_modules` dir and reinstalling should put flatpickr in the root `node_modules` dir, or you can import from `react-flatpickr/node_modules/flatpickr` manually.


### API

Every [Flatpickr](https://flatpickr.js.org/) configuration option is available.
You can check out every option [here](https://flatpickr.js.org/options/).
You can also set themes via the `theme` attribute. Learn more about the options [here](https://flatpickr.js.org/themes/).

### License
- MIT

**I'm new to Preact, so don't bite my head off. 😊**
