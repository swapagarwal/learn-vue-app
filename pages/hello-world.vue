<template>
  <div class='tutorial'>
    <h2>Hello {{ name }}! Welcome to learn-vue-app.</h2>
    <br>
    What's your name? <input v-model='name'>
    <br><br>
    This page (or rather the whole website) is rendered using Vue. Try changing the value in the above input and you'll see it reflected in the greeting message.
    <br><br>
    <h2>Brownie Tasks</h2>
    <ol>
      <li>
        Install devtools (<a href='https://chrome.google.com/webstore/detail/vuejs-devtools/nhdogjmejiglipccpnnnanhbledajbpd' target='_blank'>Chrome</a> | <a href='https://addons.mozilla.org/en-US/firefox/addon/vue-js-devtools/' target='_blank'>Firefox</a>)
      </li>
      <li>
        Right click in the browser, click on "Inspect Vue component" and open the Vue tab.
      </li>
      <li>
        Make sure the "PagesHelloWorld" line is selected.
      </li>
      <li>
        Edit the variable "name" in the section on your right hand side.
        <br>
        OR
        <br>
        Switch to the console and change the name to something else (using $vm0.name = "bar";).
        <br>
      </li>
      <li>
        You'll see the updated greeting message on the page.
      </li>
    </ol>
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
