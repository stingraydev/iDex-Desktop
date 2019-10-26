<template>
  <div class="month-block-item">
    <div class="wrapper-svg">
      <svg width="48" height="21">
        <svg x="0" y="0" width="18" height="21">
          <rect x="0" y="9" width="8" height="12" fill="#EAF9FF"></rect>
        </svg>
        <svg x="10" y="0" width="18" height="21">
          <rect x="0" y="0" width="8" height="18" fill="#EAF9FF"></rect>
          <rect class="vacancy" @mouseover="mouseOver" x="0" y="18" width="8" height="3" fill="#1EBEB4"></rect>
        </svg>
        <svg x="20" y="0" width="18" height="21">
          <rect class="vacancy" @mouseover="mouseOver" x="0" y="0" width="8" height="21" fill="#1EBEB4"></rect>
        </svg>
        <svg x="30" y="0" width="18" height="21">
          <rect class="vacancy" @mouseover="mouseOver" x="0" y="0" width="8" height="21" fill="#1EBEB4"></rect>
        </svg>
        <svg x="40" y="0" width="18" height="21">
          <rect x="0" y="0" width="8" height="3" fill="#EAF9FF"></rect>
          <rect x="0" y="3" width="8" height="9" fill="#F16953"></rect>
        </svg>
      </svg>
      <div class="pop-up" v-show="active">
        <div class="top-block">
          <img src="../assets/photo-2.png" alt="">
          <span>Катерина Иванова</span>
        </div>
        <div class="bottom-block">
          <svg x="0" y="0" width="12" height="16">
            <rect x="0" y="0" width="12" height="16" fill="#1EBEB4"></rect>
          </svg>
          <span class="bottom-block_data">09.08.2019 - 23.08.2019 (14д.)</span>
        </div>
        <span class="bottom-block_vacancy">отпуск</span>
        <button class="pop-up_button" @click="closePopUp" type="button"></button>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "bars",
    data() {
      return {
        active: false
      }
    },
    methods: {
      mouseOver: function () {
        this.active = !this.active;
      },
      closePopUp: function () {
        this.active = false;
      }
    }
  }
</script>

<style scoped>
  .month-block-item {
    display: flex;
    align-items: center;
  }

  svg {
    display: flex;
    flex-wrap: nowrap;
  }

  .vacancy:hover {

  }

  .wrapper-svg {
    position: relative;
  }
  .pop-up {
    position: absolute;
    width: 345px;
    height: 146px;
    background-color: #ffffff;
    box-shadow: 0 0 4px rgba(107, 107, 107, 0.5);
    box-sizing: border-box;
    top: 50px;
    left: -140px;
    z-index: 100;
    padding: 16px;
    border-radius: 4px;
  }

  .top-block {
    display: flex;
    align-items: center;
  }

  .top-block span {
    font-weight: 700;
    font-size: 14px;
    line-height: 20px;
    color: #000000;
    width: 71px;
    height: 38px;
    margin-left: 16px;
  }

  .bottom-block {
    margin-top: 16px;
    display: flex;
    align-items: center;
  }

  .bottom-block_data {
    font-size: 14px;
    color: #000000;
    font-weight: 400;
    margin-left: 8px;
  }

  .bottom-block_vacancy {
    margin-left: 20px;
    margin-top: 2px;
    font-size: 14px;
    line-height: 19px;
    color: #AEAEAE;
  }

  .pop-up_button {
    position: absolute;
    right: 16px;
    top: 16px;
    width: 16px;
    height: 16px;
    background: url("../assets/ic-close.svg") no-repeat;
    background-position: center center;
    border: none;
    cursor: pointer;
  }
</style>