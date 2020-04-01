<template>
  <div id="app">
    <CText typo="p" weight="bold">CText</CText>
    <CText typo="p" weight="medium">CText</CText>
    <CText typo="p" weight="semi">CText</CText>
    <CText typo="p" weight="light">CText</CText>
    <Section title="Section"></Section>
    <CIcon icon="git"/>
    <CIcon icon="css"/>
    <CIcon icon="html"/>
    <CIcon icon="php"/>
    <CIcon icon="java"/>
    <CIcon icon="javascript"/>
    <CIcon icon="nuxt"/>
    <CIcon icon="vue"/>
    <CIcon icon="phone"/>
    <CIcon icon="linkedin"/>
    <CIcon icon="mail"/>
    <CIcon icon="github"/>
    <InlineItem :text="InlineItem.text" :iconItem="InlineItem.iconItem"></InlineItem>
    <Item v-bind="Item"></Item>
  </div>
</template>

<script>
import {
  CText,
  Section,
  CIcon,
  InlineItem,
  Item,
} from './components'

export default {
  name: 'App',
  components: {
    CText,
    Section,
    CIcon,
    InlineItem,
    Item,
  },
  data () {
    return {
      InlineItem: {
        iconItem: {
          icon: 'github',
          size: 20,
          color: 'primary',
        },
        text: 'Github',
      },
      Item: {
        title: 'Desarrollador web',
        center: 'Waavi Studio',
        startDate: 'Marzo 2019',
        endDate: 'Marzo 2020',
        description: `Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aliquam lacinia sapien vel risus
                      rutrum feugiat. Donec fermentum magna est, quis placerat neque interdum quis. Mauris quis
                      dolor vitae justo imperdiet tempor id sed augue. Ut aliquet tincidunt tempus. In a auctor
                      justo, quis accumsan quam. Cras pellentesque scelerisque dictum.`,
      }
    }
  }
}
</script>

