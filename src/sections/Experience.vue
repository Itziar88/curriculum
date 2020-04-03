<template>
    <div class="Experience">
        <Section
            title="Experiencia Laboral"
        />
        <Item
            v-for="(item, index) in experiences"
            :key="index"
            v-bind="item"
        />
    </div>
</template>

<script>
import { Section, Item } from '@/components'
import VueTypes from 'vue-types'

export default {
    name: 'Experience',
    components: {
        Section,
        Item,
    },
    props: {
        experiences: VueTypes.arrayOf(VueTypes.shape({
            title: VueTypes.string,
            center: VueTypes.string,
            startDate: VueTypes.string,
            endDate: VueTypes.string,
            description: VueTypes.string,
        })).loose,
    }
}
</script>