# react-navigation-transitions

### Installation

| Package Manager |                      Command                      |
| :-------------: | :-----------------------------------------------: |
|     **npm**     | `npm install react-navigation-transitions --save` |
|    **yarn**     |  `yarn add install react-navigation-transitions`  |

### Instructions

These functions are meant to be used as the `transitionConfig` with [react-navigation](https://reactnavigation.org/). So far it includes the following transitions:

- `fromLeft`

- `fromBottom`

- `fromTop`

- `fadeIn`

- `zoomIn`

- `zoomOut`

- `flipY`

- `flipX`

More will be added in future versions.

### Usage

```javascript
import { createStackNavigator } from "react-navigation";
import { fromLeft } from "react-navigation-transitions";

const appStack = createStackNavigator(
  {
    ScreenA: {
      screen: ScreenA
    },
    ScreenB: {
      screen: ScreenB
    }
  },
  {
    initialRouteName: "ScreenA",
    transitionConfig: () => fromLeft()
  }
);
```

The default duration is `300` milliseconds but you can pass is a custom transition duration like so:

```javascript
transitionConfig: () => fromLeft(1000),
```

## Transitions

|                   fromLeft                   |                   fromBottom                   |                   fromTop                   |                   fadeIn                   |
| :------------------------------------------: | :--------------------------------------------: | :-----------------------------------------: | :----------------------------------------: |
| <img src="./gifs/from-left.gif" width="250"> | <img src="./gifs/from-bottom.gif" width="250"> | <img src="./gifs/from-top.gif" width="250"> | <img src="./gifs/fade-in.gif" width="250"> |
|                      .                       |                       .                        |                      .                      |                     .                      |
|                  **zoomIn**                  |                  **zoomOut**                   |                  **flipY**                  |                 **flipX**                  |
|  <img src="./gifs/zoom-in.gif" width="250">  |  <img src="./gifs/zoom-out.gif" width="250">   |  <img src="./gifs/flip-y.gif" width="250">  | <img src="./gifs/flip-x.gif" width="250">  |

## More references

The basis for these functions can be found in the `react-navigation` docs [here](https://reactnavigation.org/docs/stack-navigator.html#modal-stacknavigator-with-custom-screen-transitions).
