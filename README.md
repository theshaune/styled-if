# styled-if


[![GitHub issues](https://img.shields.io/github/issues/theshaune/styled-if.svg)](https://github.com/theshaune/styled-if/issues)
[![GitHub license](https://img.shields.io/github/license/theshaune/styled-if.svg)](https://github.com/theshaune/styled-if/blob/master/LICENSE)


Styled If is a simple function that helps you organize code in [styled-components](https://github.com/styled-components/styled-components). 

If a prop is defined on the component and matched then the css in the style parameter will be applied.

## Installation

```
npm install styled-if --save
```

## Usage

```js
styledIf(match: string, styles: string);
```

```js
import styled, { css } from 'styled-components';
import styledIf from 'styled-if';
  
const Title = styled.h1`
  color: palevioletred;

  ${styledIf('highlighted', css`
    border-bottom: 1px solid papayawhip;
    text-decoration: underline;
  `)}
`;

export default () => (
  <Title highlighted>
    I am a highlighted Title.
  </Title>
);
```
