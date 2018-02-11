<template>
  <div v-show="showPopup" ></div>
</template>
<script>
export default {
  name: 'popup',
  data () {
    return {
      showPopup: true
    }
  },
  methods: {
    showMe: function (e) {
      console.log('aaa')
      console.log(e)
    }
  }
}
</script>

<style lang="stylus" scoped>
</style>
