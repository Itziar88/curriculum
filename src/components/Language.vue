<template>
    <div class="Language">
        <div class="Texts">
            <CText>{{name}}</CText>
            <CText>{{level}}</CText>
        </div>
        <ProgressBar :percentage="percentage"></ProgressBar>
    </div>
</template>

<script>
import { ProgressBar, CText } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Language',
    components: {
        ProgressBar,
        CText,
    },
    props: {
        percentage: VueTypes.number,
        name: VueTypes.string,
        level: VueTypes.string,
    }
}
</script>

<style lang="scss" scoped>
@import '@/theme/theme.scss';

.Texts {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>