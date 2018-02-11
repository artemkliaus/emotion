<template>
  <div class="hamburger">
    <img src="../assets/hamburger.png" alt="menu" class="hamburger__image" v-on:click="toggleMenu">
    <transition name="fade">
      <div v-show="show" class="hamburger__menu">
        <ul class="hamburger__list">
          <li class="hamburger__list-item">
            <img src="../assets/hamburger.png" alt="menu" class="hamburger__image" v-on:click="toggleMenu">
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link"><img src="../assets/eye_header.png" class="hamburger__image"></a>
          </li>
          <li class="hamburger__list-item">
            <a href="#who" class="hamburger__list-item-link">кому полезно</a>
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link">ведущий</a>
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link">программа</a>
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link">результаты</a>
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link">как проходит</a>
          </li>
          <li class="hamburger__list-item">
            <a href="" class="hamburger__list-item-link">отзывы</a>
          </li>
        </ul>
      </div>
    </transition>
  </div>
</template>
<script>
export default {
  name: 'hamburger',
  data () {
    return {
      message: 'Вы загрузили эту страницу в: ',
      show: false,
      toggleMenu: () => {
        if (this.show) {
          this.show = false
        } else {
          this.show = true
        }
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .hamburger {
    display inline-block
    vertical-align top

    &__image {
      cursor pointer
      position relative
      top 7px
      z-index 10
    }

    &__menu {
      position absolute
      z-index 10
      top 20px
      left 0
      width 100%
      height 80px
      background-color #fff
      box-shadow 0 0 5px gray
      line-height 80px
      padding-left 15px
    }

    &__list {

      &-item {
        display inline-block
        vertical-align top
        font-size 18px
        margin-right 15px

        &-link {
          color #000
          text-decoration none
        }
      }
    }
  }

  .fade {

    &-enter-active,
    &-leave-active {
      transition: margin-left .8s;
    }

    &-enter {
      margin-left -100%

      &-to {
        margin-left 0%
      }
    }

    &-leave {
      margin-left 0%

      &-to {
          margin-left 100%
        }
      }
  }
</style>
