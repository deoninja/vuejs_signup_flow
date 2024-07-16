<template>
  <div class="container">
    <section class="step-indicator">
      <div class="step step1 active">
        <div class="step-icon">1</div>
        <p>Setup an account</p>
      </div>
      <div class="indicator-line active"></div>
      <div class="step step2">
        <div class="step-icon">2</div>
        <p>Done</p>
      </div>
    </section>
  </div>
</template>

<script>
  export default {
    props: {
      currentStep: {
        type: Number,
        required: true
      }
    }
  };
</script>

<style scoped lang="less">
  @import '../styles/variables.less';
    .container {
    max-width: 1200px;
    margin: 0 auto;
  }

  .step-indicator {
    margin-top: 50px;
    display: flex;
    align-items: center;
    padding: 0 40px;

  }

  .step {
    display: flex;
    align-items: center;
    flex-direction: column;
    position: relative;
    z-index: 1;


  }

  .step-indicator .step-icon {
   height: 30px;
    width: 30px;
    border-radius: 50%;
    background: #c2c2c2;
    font-size: 10px;
    text-align: center;
    color: #ffffff;
    position: relative;
    line-height: 30px;
    font-size: 12px;
  }

  .step.active .step-icon {
    background: @blue;
  }

  .step p {
    text-align: center;
    position: absolute;
    bottom: -40px;
    color: #c2c2c2;
    font-size: 14px;
    font-weight: bold;
    width: max-content;
  }

  .step.active p {
    color: @blue;
  }

  .step.step2 p,
  .step.step3 p {
    left: 50%;
    transform: translateX(-50%);
  }

  .indicator-line {
    width: 100%;
    height: 2px;
    background: #c2c2c2;
    flex: 1;
  }

  .indicator-line.active {
    background: @light-blue;
  }

  @media screen and (max-width: 500px) {
    .step p {
      font-size: 11px;
      bottom: -20px;
    }
  }
</style>
