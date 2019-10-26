<template>
  <div class="wrapper-person">
    <div class="person">
      <div class="person-data-block">
        <div class="person__icon">
          <img width="32" height="32"
               v-for="(item, index) in sources"
               :key="index"
               :src="item.path">
        </div>
        <div class="person__name">Иван Иванов</div>
        <div class="person__days">14/28</div>
      </div>
      <div class="month-block">
        <component v-for="(item, index) in components" :is="item.bars" v-bind:key="index"></component>
      </div>
    </div>
  </div>
</template>

<script>
  import barsGrey from "./barsGrey";
  import barsBlue from "./barsBlue";
  import barsVacancy from "./barsVacancy";

  export default {
    name: "personIvan",
    props: ['person', 'bar'],
    components: {
      barsBlue: barsBlue,
      barsGrey: barsGrey,
      barsVacancy: barsVacancy
    },
    data() {
      return {
        components: [
          {bars: 'barsGrey'},
          {bars: 'barsGrey'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsBlue'},
          {bars: 'barsVacancy'}
        ],
        sources: {
          1: {
            path: require('../assets/photo.png')
          }
        }
      }
    }
  }
</script>

<style scoped>
  .person {
    display: flex;
    margin-top: 8px;
    font-size: 12px;
    color: #232323;
    line-height: 12px;
    padding-bottom: 8px;
    border-bottom: solid 1px #F7F7F7;
  }

  .person-data-block {
    display: flex;
    width: 152px;
  }

  .person__icon {
    width: 32px;
    height: 32px;
  }

  .person__name {
    display: flex;
    align-items: center;
    width: 45px;
    margin-left: 8px;
  }

  .person__days {
    display: flex;
    align-items: center;
    justify-content: center;
    padding-left: 32px;
  }

  .month-block {
    display: flex;
    justify-content: space-between;
    margin-left: 24px;
    flex-grow: 2;
  }
</style>