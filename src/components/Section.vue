<template>
    <div class="Section">
        <CText 
            typo="h2"
            weight="semi"
            uppercase
        >
            {{ title }}
        </CText>
    </div>
</template>

<script>
import VueTypes from 'vue-types'
import { CText } from '@/components'

export default {
    name: 'Section',
    components: {
        CText,
    },
    props: {
        title: VueTypes.string.def(''),
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.Section {
    padding-bottom: 5px;
    position: relative;
    &::after {
        content: '';
        position: absolute;
        left: 0;
        bottom: 0;
        width: 100%;
        height: 4px;
        border-radius: 5px;
        background-color: $primary;
    }
}
</style>