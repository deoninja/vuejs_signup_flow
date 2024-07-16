<template>
  <div id="app">
    <StepsIndicator />
    <div class="container">
      <div class="content">
        <SignUpForm class="column left" />
        <MarketingContainer class="column right" />
      </div>
      <PhoneNumberComponent />
    </div>
  </div>
</template>

<script>
  import SignUpForm from './components/SignUpForm.vue';
  import MarketingContainer from './components/MarketingContainer.vue';
  import PhoneNumberComponent from './components/PhoneNumberComponent.vue';
  import StepsIndicator from './components/StepsIndicator.vue';

  export default {
    name: 'App',
    components: {
      SignUpForm,
      MarketingContainer,
      PhoneNumberComponent,
      StepsIndicator
    }
  };
</script>

<style lang="less">
  @import './styles/variables.less';

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;

    .container {
      max-width: 1280px;
      margin: 0 auto;
      // display: flex;
      // flex-direction: column;
      // align-items: center;

      .content {
        display: flex;
        justify-content: space-between;
        width: 100%;
        margin: 20px 0;

        @media (max-width: 1280px) {
          flex-direction: column;
        }
      }
    }
    .content {
            display: flex;
            flex-direction: row;
            width: 100%;
            height: 100vh;
            margin-top: 10em;
        }

        .column {
            flex: 1;
            padding: 20px;
            box-sizing: border-box;
            margin: 2em;
        }

        .left {
            background-color: #f0f0f0cb;
        }

        .right {
            background-color:@light-yellow;
        }
  }
</style>
