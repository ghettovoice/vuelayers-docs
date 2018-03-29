# Quick start

!> VueLayers works with Vue.js **2.3+** and OpenLayers **3.14+**

### NPM

Install latest **stable version**

```bash
npm install vuelayers
``` 

The upcoming **next version** can be installed by adding `@next` tag

```bash
npm install vuelayers@next
```  

### CDN

Recommended: [unpkg](https://unpkg.com/)  
You can browse the source of the npm package at [unpkg.com/vuelayers/](https://unpkg.com/vuelayers@latest/).

!> **OpenLayers doesn't included into package**, so you should add it yourself  

```html
<!-- include Vue -->
<script src="https://unpkg.com/vue/dist/vue.js"></script>
<!-- include OpenLayers -->
<script src="https://unpkg.com/openlayers/dist/ol.js"></script>
<!-- include UMD VueLayers build -->
<link rel="stylesheet" href="https://unpkg.com/vuelayers/lib/style.css">
<script src="https://unpkg.com/vuelayers/lib/index.umd.js"></script>

<script>
  // ...
</script>
```

**Compressed files** are also available

```html
<!-- include optimized UMD VueLayers build -->
<link rel="stylesheet" href="https://unpkg.com/vuelayers/lib/style.min.css">
<script src="https://unpkg.com/vuelayers/lib/index.umd.min.js"></script>
```


### Build from source

!> Node **v6+** is required

```bash
# clone the repo
git clone --recursive -j8 https://github.com/ghettovoice/vuelayers.git

# install dependencies
cd vuelayers
npm install

# build all targets
npm run build
# or only what you need, --format argument accepts list of target formats
# separated by comma (es, cjs, umd)
npm run rollup -- --format es,cjs

# check lib dir, there are all ready to use components
ls -l lib
```
