<template>
    <div class="InlineItem">
        <CIcon v-bind="iconItem"></CIcon>
        <CText>{{ text }}</CText>
    </div>
</template>

<script>
import { CText, CIcon } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'InlineItem',
    components: {
        CText,
        CIcon,
    },
    props: {
        iconItem: VueTypes.shape({
            icon: VueTypes.string,
            color: VueTypes.string,
            size: VueTypes.number,
        }),
        text: VueTypes.oneOfType([VueTypes.string, VueTypes.number]),
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.InlineItem {
    display: flex;
    align-items: center;
    .CIcon {
        margin-right: 5px;
    }
}
</style>