# vl-map

> The core component of VueLayers

The `vl-map` component is a part of **Map** module. It is a main container for 
all other VueLayers components and has one `default` slot to place them all. 
Usually you will use it together with [`vl-view`](component/view.md) component 
to setup `zoom`, `center`, `projection` and other view related propeties for the map.

## Versions

* [ES2015 module](https://unpkg.com/vuelayers@0.10.0-beta.6/lib/_esm2015/map/)
* [CommonJS module](https://unpkg.com/vuelayers@0.10.0-beta.6/lib/map/)

## Installation

```js
import Vue from 'vue'
import { Map } from 'vuelayers'
import 'vuelayers/lib/style.css'
// registers vl-map and vl-view components
Vue.use(Map)
```

## Properties

### controls

- **Type**: `Object, boolean`
- **Default**: `true`

Options for default controls added to the map by default. Set to `false` to disable 
all map controls. Object value is used to configure controls.

### keyboard-event-target

- **Type**: `string, Element, Document`
- **Defalt**: `this.$el`

The element to listen to keyboard events on. For example, if this option is set 
to `document` the keyboard interactions will always trigger. If this option is 
not specified, the element the library listens to keyboard events on is the 
component root element.

### load-tiles-while-animating

- **Type**: `boolean`
- **Default**: `false`

When set to `true`, tiles will be loaded during animations.

### load-tiles-while-interacting

- **Type**: `boolean`
- **Default**: `false`

When set to `true`, tiles will be loaded while interacting with the map.

### logo

- **Type**: `boolean, string, Object, Element`

The map logo. If a **string** is provided, it will be set as the image source of the 
logo. If an **object** is provided, the `src` property should be the URL for an image 
and the `href` property should be a URL for creating a link. If an **element** is provided, 
the element will be used. To disable the map logo, set the option to `false`. 
By default, the OpenLayers logo is shown.

### move-tolerance

- **Type**: `number`
- **Default**: `1`

The minimum distance in pixels the cursor must move to be detected as a map move 
event instead of a click. Increasing this value can make it easier to click on the map.

### pixel-ratio

- **Type**: `number`
- **Default**: `1`

The ratio between physical pixels and device-independent pixels (dips) on the device.

### renderer

- **Type**: `string, string[]`
- **Default**: `['canvas', 'webgl']`

The map renderer. By default, **Canvas** and **WebGL** renderers are tested for support in that order, 
and the first supported used. 

### tabindex

- **Type**: `number`

Root element `tabindex` attribute value. Value should be provided to allow 
keyboard events on map.