<div align="center">
  
# :iphone: Easy Ref Merge :fist:

:blue_book: **[Description](#description)**

:boom: **[ShowCase](#showcase)**

:zap: **[Installation](#installation)**

:key: **[Usage](#usage)**

:page_facing_up: **[Examples](#examples)**

:ok_hand: **[Why easy-ref-merge ?](#why-easy-ref-merge-)**

[![Twitter Follow](https://img.shields.io/twitter/follow/HossamElgzeery?label=Follow%20Me&style=social)](https://www.twitter.com/HossamElgzeery)

</div>

# Description

easy ref merge is a react/react-native package that helps you to merge more than one reference and inject them to the same component.

# Installation

```
#npm
npm install easy-ref-merge

#yarn
yarn add easy-ref-merge

```

# Usage

**We have only one function**

- **refsMerge** its called with any number of references and produce single merged reference.

## Package Import :

```javascript
import refsMerge from "easy-ref-merge";
```

# Examples

**./OuterWrapper.js**

```javascript
import InnerWrapper from "./InnerWrapper.js";
import React, { useRef } from "react";
const OuterWrapper = () => {
  const ref = useRef();
  return <InnerWrapper ref={ref} />;
};
```

**./InnerWrapper.js**

```javascript
import React from 'react';
import {Text} from 'react-native'
import refsMerge from "easy-ref-merge";
const InnerWrapper=React.forwardRef((props, ref)=>
{
  const localRef=//a reference generated for special purpose
  return <Text ref={refsMerge(localRef,ref)}>Easy Ref Merge</Text>
},[]);

```

# Why easy-ref-merge ?

- :heavy_check_mark: small size package :muscle:
- :heavy_check_mark: easy to use :muscle:
- :heavy_check_mark: allows you to merge any number of references :muscle:
