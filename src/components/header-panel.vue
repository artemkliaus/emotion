<template>
  <div class="header-row">
    <hamburger></hamburger>
    <span>
      <img src="../assets/eye_header.png" class="header-row__image">
      <span class="header-row__text">неврозы мегаполиса</span>
    </span>
    <call-button v-bind="callButtonProps" class="isDashed" v-on:showPopup="showMe"></call-button>
    <div class="header-row__number-block">
      <span class="header-row__number">8 800 550-59-66</span>
      <span class="header-row__number-text">Звонок по России бесплатный</span>
    </div>
  </div>
</template>
<script>
import Hamburger from './hamburger.vue'
import CallButton from './call-button.vue'
export default {
  name: 'header-panel',
  data () {
    return {
      message: 'Вы загрузили эту страницу в ' + new Date().toLocaleString(),
      callButtonProps: {
        text: 'Заказать звонок',
        isInline: true,
        isDashed: true
      },
      showMe: function () {
        console.log('header')
      }
    }
  },
  components: {
    Hamburger,
    CallButton
  }
}
</script>

<style lang="stylus" scoped>

  .header-row {
    display grid
    grid-template-columns 100px 1fr 151px 225px
    padding-top 45px

    &__text {
      font-size 21px
      text-transform uppercase
    }

    &__image {
      position relative
      top 3px
      margin-right 8px
    }

    &__number {

      &-block {
        margin-left 55px
      }

      color #fff
      display block
      font-size 21px
      font-weight 600

      &-text {
        color #fff
        font-weight 200
      }
    }
  }

</style>
