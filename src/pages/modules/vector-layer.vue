<template lang="pug">
  div(':class'="[$options.name]")
    vld-hero(':bold'="true" color="is-info")
      h1.title Vector layer
      h2.subtitle Components for vector layers

    section.section
      vld-cmp-api(':api'="layerApi")
</template>

<script>
  import { constant } from 'lodash/fp'
  import layerApi from '../../api/vector-layer/layer'

  const computed = {
    layerApi: constant(layerApi),
  }

  export default {
    name: 'vld-vector-layer-doc',
    computed,
  }
</script>

<style>
</style>
