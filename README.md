# react-navigation-transitions

### Installation
`npm install react-navigation-transitions --save`

### Instructions
These functions are meant to be used as the `transitionConfig` with [react-navigation](https://reactnavigation.org/). So far it includes the following transitions:

`fromLeft`

`fromTop`

`fadeIn`

`zoomIn`

`zoomOut`

`flipY`

`flipX`

More will be added in future versions.

### Example

```javascript
import { StackNavigator } from 'react-navigation';
import { fromLeft } from 'react-navigation-transitions';

const appStack = StackNavigator(
  {
    ScreenA: {
      screen: ScreenA,
    },
    ScreenB: {
      screen: ScreenB,
    },
  },
  {
    initialRouteName: 'ScreenA',
    transitionConfig: () => fromLeft(),
  },
);
```

The default duration is 300 milliseconds but you can pass is a custom transition duration like so:

```javascript
transitionConfig: () => fromLeft(1000),
```

## GIFS

### fromLeft

![](./gifs/from-left.gif)

### fromTop

![](./gifs/from-top.gif)

### fadeIn

![](./gifs/fade-in.gif)

### zoomIn

![](./gifs/zoom-in.gif)

### zoomOut

![](./gifs/zoom-out.gif)

### flipY

![](./gifs/flip-y.gif)

### flipX

![](./gifs/flip-x.gif)

The basis for these functions can be found in the `react-navigation` docs [here](https://reactnavigation.org/docs/stack-navigator.html#modal-stacknavigator-with-custom-screen-transitions).
