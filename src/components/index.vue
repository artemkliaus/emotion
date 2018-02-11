<template>
  <div v-on:showPopup="showMe">
    <header-panel v-on:showPopup="showMe"></header-panel>
    <first-section></first-section>
    <second-section></second-section>
    <popup></popup>
  </div>
</template>

<script>
import HeaderPanel from './header-panel.vue'
import FirstSection from './first-section.vue'
import SecondSection from './second-section.vue'
import Popup from './popup.vue'

export default {
  name: 'Index',
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    showMe: function () {
      console.log('index')
    },
    showPopup: function () {
      console.log('index')
    }
  },
  components: {
    HeaderPanel,
    FirstSection,
    SecondSection,
    Popup
  }
}
</script>

<style scoped>
</style>
