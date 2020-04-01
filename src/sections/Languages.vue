<template>
    <div class="Languages">
        <CText
            typo="h4"
            weight="medium"
            uppercase
        >
            Languages
        </CText>
        <div
            v-for="(item, index) in info"
            :key="index"
            class="Item"
        >
            <Language
                v-bind="item"
            />
        </div>
    </div>
</template>

<script>
import { CText, Language } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Languages',
    components: {
        CText,
        Language,
    },
    props: {
        info: VueTypes.arrayOf(VueTypes.shape({
            language: VueTypes.shape({
                percentage: VueTypes.number,
                name: VueTypes.string,
                level: VueTypes.string,
            }),
        })).loose,
    }
}
</script>

<style lang="scss" scoped>
.Item {
    padding: 10px 0 0 5px;
}
</style>