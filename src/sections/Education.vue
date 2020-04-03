<template>
    <div class="Education">
        <Section
            title="Formación Académica"
        />
        <Item
            v-for="(item, index) in studies"
            :key="index"
            v-bind="item"
        />
    </div>
</template>

<script>
import { Section, Item } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Education',
    components: {
        Section,
        Item,
    },
    props: {
        studies: VueTypes.arrayOf(VueTypes.shape({
            title: VueTypes.string,
            center: VueTypes.string,
            startDate: VueTypes.string,
            endDate: VueTypes.string,
        })).loose,
    }
}
</script>