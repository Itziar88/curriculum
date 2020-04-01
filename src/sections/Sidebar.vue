<template>
    <div class="Sidebar">
        <Contact :info="contact" />
        <Technologies :info="technologies" />
        <Languages :info="languages" />
    </div>
</template>

<script>
import {
  Contact,
  Technologies,
  Languages,
} from '@/sections'
import VueTypes from 'vue-types'

export default {
  name: 'Sidebar',
  components: {
    Contact,
    Technologies,
    Languages,
  },
  props: {
      contact: VueTypes.array,
      technologies: VueTypes.array,
      languages: VueTypes.array,
  }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.Sidebar {
    widows: 100%;
    padding: 25px;
    background-color: $secondary;
    .Contact,
    .Technologies,
    .Languages {
        margin-top: 15px;
    }
}
</style>
