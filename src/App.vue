<template>
  <div id="app">
    <div class="container">
      <StepsIndicator />
      <div class="content">
        <SignUpForm />
        <MarketingContainer />
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
      display: flex;
      flex-direction: column;
      align-items: center;

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
  }
</style>
