<template>
  <div class="marketing-container">
    <!-- Marketing content here (placeholders for now) -->
    <div class="content"></div>
  </div>
</template>

<script>
  export default {
    name: 'MarketingContainer'
  };
</script>

<style scoped lang="less">
  @import '../styles/variables.less';

  .marketing-container {
    max-width: 500px;
    background: @light-yellow;
    padding: 20px;
    border-radius: 5px;
    position: relative;
    overflow: hidden;

    .content {
      position: relative;
      z-index: 1;
    }

    &::before {
      content: '';
      position: absolute;
      bottom: 0;
      right: 0;
      top: 10%;
      width: 100%;

      height: 100%;
      background: linear-gradient(-15deg, @bright-yellow 50%, transparent 50%);
      z-index: 0;
    }


    h2 {
      margin-bottom: 10px;
    }


  }
</style>
