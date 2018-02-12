# styled-skeleton

Single file with skeleton.css for your [styled-components](https://styled-components.com/)

Original skeleton.css copied and adapted from [dhg/Skeleton](https://github.com/dhg/skeleton)

Structure borrowed from [styled-normalize](https://github.com/sergeysova/styled-normalize)


## Usage

```bash
yarn add styled-skeleton styled-components
```

### JavaScript

```javascript
// ----- styles/index.js
import styledSkeleton from 'styled-skeleton';
import { injectGlobal } from 'styled-components';

export default () => injectGlobal`
  ${styledSkeleton}

  body {
    padding: 0;
    background-color: pink;
  }
`;

// ----- client.js
// ... imports
import baseStyles from './styles/index';

const render = () => {
  baseStyles();

  ReactDOM.render(<AppContainer />, document.getElementById('app-root'));
};

render();
```

With named import

```js
// ES Modules
import { skeleton, version } from 'styled-skeleton';

// CommonJS
const { skeleton, version } = require('styled-skeleton');
```

## ServerSide Rendering

Styled-components supports SSR, you can [read discussion](https://github.com/styled-components/styled-components/issues/386) or [open RURARAR](https://github.com/lestad/rurarar/)
