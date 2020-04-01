<template>
  <div id="app" class="Container">
    <Sidebar 
      :contact="cv.contact"
      :technologies="cv.technologies"
      :languages="cv.languages"
    ></Sidebar>
    <div class="Body">body</div>
  </div>
</template>

<script>
import { default as cv } from './cv'

import {
  Sidebar,
} from './sections'

export default {
  name: 'App',
  components: {
    Sidebar,
  },
  data () {
    return {
      cv,
    }
  }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.Container {
  display: flex;
  position: relative;
  width: 100%;
  box-sizing: border-box;

  .Sidebar {
    flex: 1 1 33%;
  }
  .Body {
    flex: 1 1 66%;
    background-color: aliceblue;
  }
}
</style>
