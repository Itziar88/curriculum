<template>
    <div class="ProgressBar">
        <div class="Wrapper" :style="{ width: `${percentage}%`}">
        </div>
    </div>
</template>

<script>
import VueTypes from 'vue-types'

export default {
    name: 'ProgressBar',
    props: {
        percentage: VueTypes.number.def(0),
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.ProgressBar {
    height: 4px;
    background-color: $white;
    border: 1px solid $primary;
    border-radius: $border-radius;
}
.Wrapper {
    height: 100%;
    background-color: $primary;
}
</style>