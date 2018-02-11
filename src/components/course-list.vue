<template>
  <li class="course-list">
    <div class="course-list__num-block">
      <span class="course-list__number">{{id}}</span>
    </div>
    <p class="course-list__title">{{title}}</p>
    <p class="course-list__description">{{descr}}</p>
  </li>
</template>
<script>
export default {
  name: 'course-list',
  props: ['id', 'title', 'descr']
}
</script>

<style lang="stylus" scoped>
  .course-list {
    display inline-block
    vertical-align top
    width 250px
    height 240px
    padding-right 50px

    &__number {
      display inline-block
      width 50px
      height 50px
      font-size 20px
      border 1px solid #4109ff
      border-radius 50%
      text-align center
      line-height 50px
      margin-bottom 10px
    }

    &__title {
      font-size 18px
      font-weight 900
    }

    &__description {
      font-size 15px
      color #7d7d7d
    }
  }
</style>
