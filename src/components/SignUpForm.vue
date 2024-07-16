<template>
  <div class="form-container">
    <h2>Lorem ipsum dolor sit amet</h2>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    <form>
      <!-- Form fields here (placeholders for now) -->
    </form>
  </div>
</template>

<script>
  export default {
    name: 'SignUpForm'
  };
</script>

<style scoped lang="less">
  @import '../styles/variables.less';

  .form-container {
    max-width: 700px;
    background-color: white;
    padding: 20px;
    border-radius: 5px;
  }
</style>
