<template>
  <section class="second-section">
    <h2 class="second-section__title" id="who">кому будет полезен курс?</h2>
    <ul class="second-section__list">
      <li
        is="course-list"
        v-for="item in courseList"
        v-bind:key="item.id"
        v-bind:id="item.id"
        v-bind:title="item.title"
        v-bind:descr="item.description"
      ></li>
    </ul>
  </section>
</template>
<script>
import CourseList from './course-list.vue'
export default {
  name: 'second-section',
  components: {
    CourseList
  },
  data () {
    return {
      courseList: [
        {
          id: '01',
          title: 'Если у вас панические атаки, невроз, ВСД',
          description: 'Справитесь с паническими атаками и агорафобией. Научитесь устранять проявления ВСД'
        },
        {
          id: '02',
          title: 'Испытываете тревогу и страх за здоровье',
          description: 'Уменьшите уровень вашей тревоги, научитесь взаимодействовать с фобиями и страхами'
        },
        {
          id: '03',
          title: 'Боитесь потерять контроль, сойти с ума, нанести вред',
          description: 'Устраните навязчивые мысли, избавитесь от страха потерять контроль и сойти с ума'
        },
        {
          id: '04',
          title: 'У вас проблемы на работе, в семье, личной жизни',
          description: 'Поймете в чем корень вашего невроза. Создадите пошаговый план для решения и начнете действовать'
        },
        {
          id: '05',
          title: 'Избавились от панических атак, но вам не легче',
          description: 'Обучитесь когнитивно-поведенческой терапии, будете практиковать ведение таблиц в формате РЭПТ'
        },
        {
          id: '06',
          title: 'Вы эмоционально нестабильны',
          description: 'Перестанете испытывать «негативные эмоции». Научитесь рационально реагировать на ситуации'
        },
        {
          id: '07',
          title: 'У вас череда стрессовых ситуаций',
          description: 'Повысите стрессоустойчивость и сохраните здоровое, взвешенное поведение в любой ситуации'
        },
        {
          id: '08',
          title: 'Вы не можете принять важное решение',
          description: 'Научитесь принимать решения, повысите свою эффективность и самодисциплину'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .second-section {
    display grid
    display-template-columns 305px 305px 305px 305px
    display-template-rows 130px 240px 240px

    &__title {
      font-size 35px
      font-weight 900
      color #262626
      text-transform uppercase
    }

    &__list {
      margin-top 60px
    }
  }
</style>
