<template>
    <div class="Technologies">
        <CText
            typo="h4"
            weight="medium"
            uppercase
        >
            Tecnologías
        </CText>
        <div
            v-for="(item, index) in info"
            :key="index"
            class="Item"
        >
            <InlineItem
                v-bind="item"
            />
        </div>
    </div>
</template>

<script>
import { CText, InlineItem } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Technologies',
    components: {
        CText,
        InlineItem,
    },
    props: {
        info: VueTypes.arrayOf(VueTypes.shape({
            iconItem: VueTypes.shape({
                icon: VueTypes.string,
                color: VueTypes.string,
                size: VueTypes.number.def(20),
            }),
            text: VueTypes.oneOfType([VueTypes.string, VueTypes.number]),
        })).loose,
    }
}
</script>

<style lang="scss" scoped>
.Item {
    padding: 10px 0 0 5px;
}
</style>