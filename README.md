# svelte-loading-animation
Collection of simple and light-weight CSS loading animations / spinners for [Svelte](http://svelte.dev).


## Available Loading Animations
Currently we have 7 loading animations
| Animation | Component Name | Description |
| ------ | --- | ---- |
| Bars | LoadBars | 3 vertical bars animated |
| Coin | LoadCoin | Flipping / spinning circle |
| Ellipsis | LoadEllipsis | 3 dots animated |
| Hour Glass | LoadHourGlass | Simple hour glass animation |
| Ring | LoadRing | Chasing ring animation |
| Ripple | LoadRipple | Ripple animation |
| Spinner | LoadSpinner | Basic spinner |

## Installation
```sh
npm install svelte-loading-animation
```

## Usage
First you need to import the desired animation(s) on the script section
```js
// ...
	import { LoadRing, LoadRipple } from 'svelte-loading-animation';
// ...
```
and then use it on your application. Here's some example code:
```html
  <LoadRipple />

  <LoadRing />
```
By default, they have Svelte's orange color and 64px*64px size. You can customize the looks by passing available properties.

## Properties
| Property | Default | Accepted Value |
| ----- | ----- | ------ |
| color | #ff3e00 | Any CSS background color |
| size | 64px | Integer or decimal in px, em, rem |

Some samples with props:

```html
  <LoadHourGlass size="64px" color="#d43ef1"/>
  <LoadBars size="64px" color="red"/>
  <LoadSpinner size="5.5rem" color="rgba(0,0,0,.32)"/>
```

## License
MIT

