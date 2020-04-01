<template>
    <div class="Item">
        <CText typo="h3">{{ title }}</CText>
        <div class="CenterDates">
            <CText typo="h4">{{ center }}</CText>
            <div class="Dates">
                <CText typo="h5">{{ startDate }}</CText>
                -
                <CText typo="h5">{{ endDate }}</CText>
            </div>
        </div>
        <CText align="justify">{{ description }}</CText>
    </div>
</template>

<script>
import { CText } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Item',
    components: {
        CText,
    },
    props: {
        title: VueTypes.string,
        center: VueTypes.string,
        startDate: VueTypes.string,
        endDate: VueTypes.string,
        description: VueTypes.string,
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.CenterDates {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.Dates {
    display: flex;
    justify-content: flex-end;
    align-items: center;
}
</style>