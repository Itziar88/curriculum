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
  </div>
</template>

<script>
import { 
  CText,
  Section,
  CIcon,
} from './components'

export default {
  name: 'App',
  components: {
    CText,
    Section,
    CIcon,
  }
}
</script>

