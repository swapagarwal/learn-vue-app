<template>
  <div class='tutorial'>
    <h1>
      Hello {{ name }}! Welcome to learn-vue-app.
    </h1>
    <br>
    Vue is a progressive + reactive framework.
    <br>
    TODO: Explain progressive?
    <br>
    TODO: Explain reactive?
    <br><br>
    What's your name? <input v-model='name'>
    <br><br>
    Brownie Tasks:
    <br>1. Install devtools (<a href='https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd' target='_blank'>Chrome</a> | <a href='https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/' target='_blank'>Firefox</a>)
    <br>2. Right click in the browser and click on inspect to open the console.
    <br>3. Change the name to something else and see it reflected on the page.
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: 'foo'
      }
    }
  }
</script>

<style scoped>

</style>
