<template>
  <div class="wrapper">
    <section class="desktop">
      <div class="top-panel">
        <h1 class="top-panel__title">Рабочий стол руководителя</h1>
        <div class="top-panel__tools">
          <button type="button" class="top-panel__button button-left">Dashboard</button>
          <button type="button" class="top-panel__button button-right">Team line up</button>
        </div>
        <div class="dashboard">
          <div class="dashboard__top-panel">
            <div class="dashboard__title-block">
              <h2 class="dashboard__title">График отпусков</h2>
              <div class="dashboard__switch-year">
                <button class="dashboard__button button-left"></button>
                <div>2019</div>
                <button class="dashboard__button button-right"></button>
              </div>
            </div>
            <div class="dashboard__col-name">
              <div class="col-name-block">
                <span>Фамилия, Имя</span>
                <span>дней</span>
              </div>
              <span>Янв</span>
              <span>Фев</span>
              <span>Мар</span>
              <span>Апр</span>
              <span>Май</span>
              <span>Июн</span>
              <span>Июл</span>
              <span>Авг</span>
              <span>Сен</span>
              <span>Окт</span>
              <span>Ноя</span>
              <span>Дек</span>
            </div>
          </div>
        </div>
        <component v-for="(item, index) in components" :is="item.componentName" v-bind:key="index">
          <bars></bars>
        </component>
      </div>
    </section>
  </div>
</template>

<script>
  import personIvan from "./personIvan";
  import personKate from "./personKate";
  import bars from "./barsGrey";

  export default {
    name: "desktop",
    components: {
      personIvan: personIvan,
      personKate: personKate,
      bars: bars
    },
    data() {
      return {
        components: {
         1: {
            componentName: 'personIvan',
            name: 'Иван',
            suname: 'Иванов',
            days: 14,
            src: require('../assets/photo.png')
          },
          2: {
            componentName: 'personKate',
            name: 'Катерина',
            suname: 'Иванова',
            days: 14,
            src: require('../assets/photo-2.png')
          },
          3: {
            componentName: 'personIvan',
            name: 'Иван',
            suname: 'Иванов',
            days: 14,
            src: require('../assets/photo.png')
          },
          4: {
            componentName: 'personIvan',
            name: 'Иван',
            suname: 'Иванов',
            days: 14,
            src: require('../assets/photo.png')
          },
          5: {
            componentName: 'personIvan',
            name: 'Иван',
            suname: 'Иванов',
            days: 14,
            src: require('../assets/photo.png')
          }
        }
      }
    }
  };
</script>

<style scoped>
  .wrapper {
    margin-top: 81px;
    padding-left: 100px;
    background: linear-gradient(to right, #393A3F 50%, #F7F7F7 50%);
  }

  .desktop {
    max-width: 978px;
    padding: 30px 20px 80px 20px;
    background-color: #fff;
    border: none;
  }

  .top-panel__title {
    font-family: 'Open Sans', sans-serif;
    font-style: normal;
    font-weight: 400;
    font-size: 32px;
    color: #000000;
    line-height: 40px;
    margin-left: 16px;
  }

  .top-panel__tools {
    background-color: #F7F7F7;
    margin-top: 20px;
    padding-top: 6px;
    padding-bottom: 6px;
    padding-left: 16px;
    display: flex;
    align-items: center;
  }

  .top-panel__button {
    width: 153px;
    height: 45px;
    border-radius: 2px;
    border: none;

    font-size: 14px;
    text-align: center;
    line-height: 12px;
    cursor: pointer;
  }

  .top-panel__button.button-left {
    background-color: #556080;
    color: #CACACA;;
  }

  .top-panel__button.button-right {
    background-color: #ffffff;
    color: #556080;
  }

  .dashboard {
    margin-top: 22px;
  }

  .col-name-block span:nth-child(2) {
    margin-left: 32px;
  }

  .dashboard__top-panel {
    background-color: #F7F7F7;
    padding-left: 20px;
    padding-top: 17px;
    padding-bottom: 8px;
  }

  .dashboard__title {
    font-weight: normal;
    font-size: 18px;
    color: #2D2E2E;
  }

  .dashboard__title-block {
    display: flex;
    justify-content: space-between;
  }

  .dashboard__switch-year {
    font-size: 18px;
    color: #232323;
    line-height: 12px;
    display: flex;
    align-items: center;
  }

  .dashboard__switch-year div {
    padding-left: 8px;
    padding-right: 8px;
  }

  .dashboard__button {
    width: 24px;
    height: 24px;
    border: none;
    cursor: pointer;
  }

  .dashboard__button.button-left {
    background: url("../assets/ic-left.svg") no-repeat;
    background-position: center center;
  }

  .dashboard__button.button-right {
    background: url("../assets/ic-right.svg") no-repeat;
    background-position: center center;
  }

  .dashboard__col-name {
    margin-top: 21px;
    padding-right: 20px;
    display: flex;
    justify-content: space-between;
    font-size: 10px;
    color: #232323;
    line-height: 12px;
  }
</style>
