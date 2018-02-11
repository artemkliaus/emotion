<template>
  <section class="first-section">
    <h3 class="first-section__pre-title">открыт набор на 8 сезон</h3>
    <h1 class="first-section__title">Избавься от невроза, всд<br>и страхов за 10 занятий</h1>
    <p class="first-section__description">Онлайн-курс по когнитивно-поведенческой терапии,<br>
    профилактике ВСД и неврозов который принес<br>результат уже более чем 1300 людям</p>
    <div class="first-section__info-block">
      <span class="first-section__wifi">онлайн</span>
      <span class="first-section__weeks">5 недель</span>
      <span class="first-section__lessons">10 занятий</span>
    </div>
    <div>
      <call-button v-bind="callButtonProps"></call-button>
      <span class="first-section__course-text">или получить
      <call-button text="консультацию" isInline=true class="isSolid" ></call-button>
      </span>
    </div>
    <div class="first-section__speaker-block">
      <div class="first-section__speaker-description">
          <span class="first-section__speaker-pre-title">ведущий курса</span>
          <span class="first-section__speaker-title">{{ speaker.name }}</span>
          <div class="first-section__speaker-video">
            <span class="first-section__speaker-video-pic"></span>
            <span class="first-section__speaker-text">Смотреть видеоприглашение</span>
          </div>
      </div>
    </div>
  </section>
</template>
<script>
import CallButton from './call-button.vue'
export default {
  name: 'first-section',
  components: {
    CallButton
  },
  data () {
    return {
      callButtonProps: {
        text: 'Заказать звонок',
        isButton: true
      },
      speaker: {
        name: 'Андрей Красиков'
      }
    }
  }
}
</script>

<style lang="stylus" scoped>
  .first-section {
    display grid
    grid-template-columns 1fr 410px
    grid-template-rows 50px 140px 100px 140px 200px
    margin-top 60px

    &__pre-title {
      font-size 21px
      font-weight 900
      color #b100ff
      text-transform uppercase
    }

    &__speaker-block {
      grid-column-start 2
      grid-row-start 1
      grid-row-end 6
    }

    &__title {
      font-size 46px
      font-weight 900
      color #262626
      text-transform uppercase

      &-second {
        font-size 33px
      }
    }

    &__description {
      font-size 24px
      color #7d7d7d
    }

    &__info-block {
      line-height 140px
    }

    &__info-block {
      font-size 21px
    }
    &__wifi {
      display inline-block
      width 115px

      &::before {
        content ''
        position relative
        top 5px
        display inline-block
        width 27px
        height 25px
        background-image url(../assets/f_sec_sprite.png)
        background-repeat no-repeat
        background-position center left
        background-size cover
        margin-right 10px
      }
    }

    &__weeks {
      display inline-block
      width 125px
      margin-left 35px

      &::before {
        content ''
        position relative
        top 5px
        display inline-block
        width 27px
        height 25px
        background-image url(../assets/f_sec_sprite.png)
        background-repeat no-repeat
        background-position -33px 0
        background-size cover
        margin-right 10px
      }
    }

    &__lessons {
      display inline-block
      width 155px
      margin-left 35px

      &::before {
        content ''
        position relative
        top 5px
        display inline-block
        width 27px
        height 25px
        background-image url(../assets/f_sec_sprite.png)
        background-repeat no-repeat
        background-position -64px 0
        background-size cover
        margin-right 10px
      }
    }

    &__course-text {
      margin-left 30px
    }

    &__speaker {

      &-block {
        position relative
        background-image url(../assets/speaker.png)
        background-repeat no-repeat
        background-position right bottom
        background-size contain
      }

      &-description {
        position absolute
        top 0
        bottom 0
        margin auto 0
        width 200px
        height 110px
      }

      &-pre-title {
        display block
        text-transform uppercase
        font-size 12px
        font-weight 900
        color rgba(255, 255, 255, 0.5)
      }

      &-title {
        display block
        font-size 21px
        color #fff
      }

      &-video {
        font-size 14px
        color rgba(255, 255, 255, 0.8)
        margin-top 20px

        &-pic {
          display inline-block
          width 40px
          height 40px
          background-color rgba(255, 0, 40, 0.8)
          border-radius 50%
          cursor pointer

          &:hover {
            background-color rgba(255, 0, 40, 1)
          }

          &::after {
            display inline-block
            position relative
            top 5px
            left 11px
            line-height 40px
            width 20px
            height 30px
            content ''
            background-image url(../assets/f_sec_sprite.png)
            background-repeat no-repeat
            background-position -114px 0px
            background-size cover
          }
        }
      }

      &-text {
        margin-left 6px
        margin-top 2px
        width 150px
        display inline-block
        vertical-align top
      }
    }
  }
</style>
