<template>
  <div class="month-block-item">
    <svg width="48" height="21">
      <rect width="8" height="21" fill="#F6F6F6"></rect>
      <rect x="10" width="8" height="21" fill="#F6F6F6"></rect>
      <rect x="20" width="8" height="21" fill="#F6F6F6"></rect>
      <rect x="30" width="8" height="21" fill="#F6F6F6"></rect>
      <rect x="40" width="8" height="21" fill="#F6F6F6"></rect>
    </svg>
  </div>
</template>

<script>
  export default {
    name: "bars"
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
</style>