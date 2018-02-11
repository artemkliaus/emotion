<template>
  <span v-if=isInline class="call-button__link" v-on:click="triggerPopup">{{ text }}</span>
  <button v-else-if=isButton class="call-button__button" v-on:click="triggerPopup">записаться на курс</button>
</template>
<script>
export default {
  name: 'call-button',
  props: ['text', 'isInline', 'isButton', 'isSolid', 'isDashed'],
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    triggerPopup: function () {
      this.$emit('showPopup')
      console.log('call')
    }
  }
}
</script>

<style lang="stylus" scoped>
  .call-button {

    &__link {
      display inline-block
      height 25px
      color #3b3bff
      font-size 18px
      font-weight 900
      cursor pointer
      transition color .3s linear,
      border-bottom .3s linear

      &.isDashed {
        border-bottom 2px dashed #3b3bff
      }

      &.isSolid {
        border-bottom 2px solid #3b3bff
      }

      &:hover {
        color #b400ff
        border-color #b400ff
      }
    }

    &__button {
      cursor pointer
      padding 35px 38px
      background-color #3b3bff
      border-radius 50px
      font-size 18px
      color #fff
      font-weight 900
      text-transform uppercase
      box-shadow 4px 7px 31px #3b3bff
      transition background-color .3s ease-out,
      box-shadow .5s ease-out

      &:hover {
        background-color #b400ff
        box-shadow 4px 7px 31px #b400ff
      }
    }
  }
</style>
