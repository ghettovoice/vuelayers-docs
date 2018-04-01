# vl-view

> 2D representation of the map

The `vl-view` component is a part of **Map** module. It is the component to act upon
to change the **center**, **resolution** and **rotation** of the map.

## Module system

* [ES6 module](https://unpkg.com/vuelayers@0.10.0-beta.6/lib/_esm2015/map/)
* [CommonJS module](https://unpkg.com/vuelayers@0.10.0-beta.6/lib/map/)

## Installation

Same as [`vl-map`](component/map.md) installation.

```js
import Vue from 'vue'
import { Map } from 'vuelayers'
import 'vuelayers/lib/style.css'
// registers vl-map and vl-view components
Vue.use(Map)
```

## Usage

Example of simple map. Also see documentation of [`vl-view`](component/view.md), 
[`vl-layer-tile`](component/tile-layer.md) and [`vl-source-osm`](component/osm-source.md) 
components.

<vuep template="#example"></vuep>

<script v-pre type="text/x-template" id="example">
  <template>
    <vl-map :load-tiles-while-animating="true" :load-tiles-while-interacting="true" style="height: 400px">
        <vl-view :zoom.sync="zoom" :center.sync="center" :rotation.sync="rotation"></vl-view>

        <vl-layer-tile id="osm">
            <vl-source-osm></vl-source-osm>
        </vl-layer-tile>
    </vl-map>
  </template>

  <script>
    export default {
      data () {
        return { 
          zoom: 2,
          center: [0, 0],
          rotation: 0,
        }
      },
    }
  </script>
</script>

## Properties

### center

- **Type**: `number[]`
- **Default**: `[0, 0]`

The center coordinate of the map view in the provided [`projection`](#projection).

### constrain-rotation

- **Type**: `boolean | number`
- **Default**: `true`

### data-projection

- **Type**: `string`
- **Default**: `undefined`

Projection of input/output plain coordinates in properties, events and etc (`center`, `update:center` and other).

### enable-rotation

- **Type**: `boolean`
- **Default**: `true`

### extent

- **Type**: `number[leftBottomX, leftBottomY, rightTopX, rightTopY]`
- **Default**: `undefined`

The extent that constrains the `center` defined in the view projection, in other words, 
center cannot be set outside this extent.

### max-resolution

- **Type**: `number`

### projection

- **Type**: `string`
- **Default**: `EPSG:3857`

The view internal projection. All plain coordinates (`center` property, `update:center` event and etc.) 
will be in that projection if [`data-projection`](#data-projection) property and [global data projection](quickstart.md#global-data-projection)
is `undefined`.

### resolution

- **Type**: `number`
- **Default**: `undefined`

The initial resolution for the view.

### rotation

- **Type**: `number`
- **Default**: `0`

The initial rotation for the view in **radians** (positive rotation clockwise).

### zoom

- **Type**: `number`
- **Default**: `0`

Zoom level used to calculate the resolution for the view as `int` value. 
Only used if [`resolution`](#resolution) is not defined.

## Events

## Methods