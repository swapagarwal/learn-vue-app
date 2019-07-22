<template>
  <div class='tutorial'>
    Let's start! 👊
    <br><br>
    Here's a sample HTML file:
    <pre v-highlightjs="html"><code class="html"></code></pre>
    <br>
    Now, I had promised you in the introduction that you can start small with Vue. So to add Vue here, you can just load Vue via CDN like this:
    <pre v-highlightjs="unpkg"><code class="html"></code></pre>
    <br>
    Next, we modify the "div" to include an "id" (we'll see why below) and use the "name" via template syntax (double curly braces):
    <pre v-highlightjs="el"><code class="html"></code></pre>
    <br>
    Finally, we create a Vue instance using:
    <pre v-highlightjs="app"><code class="html"></code></pre>
    <br>
    Two things to note here:
    <ol>
      <li>"el" takes the CSS selector of the element where we want to attach the Vue instance (that's why we added it before!).</li>
      <li>"data" contains the model object which will be accessible inside the element selected above.</li>
    </ol>
    <br>
    And we are done! Try this hands-on in the below exercise. I recommend you to complete this before moving on to the next tutorial. Open the file at the location mentioned on the right side and make the appropriate changes.
    <br><br>
    <Exercise/>
    Refresh the page to see the changes reflected above.
    <br><br>
    Done? Does your output (right side) match the expected output (left side)?
    <br>
    If yes, congratulations! You've successfully started your Vuetiful journey! See you in the next tutorial.
    <TutorialNavigation/>
  </div>
</template>

<script>
  import Exercise from '~/components/Exercise.vue'
  import TutorialNavigation from '~/components/TutorialNavigation.vue'
  export default {
    components: {
      Exercise,
      TutorialNavigation
    },
    data() {
      return {
        html: `<html>
    <head>...</head>
    <body>
        <div>
            <h1>Hello John Doe! Welcome to learn-vue-app.</h1>
        </div>
    </body>
</html>`,
        unpkg: `<script src="https://unpkg.com/vue"><\/script>`,
        app: `<script>
    const app = new Vue({
        el: '#baby-steps',
        data: {
            name: 'Foo Bar'
        }
    })
<\/script>`,
        el: `<div id="baby-steps">
    <h1>Hello {{ name }}! Welcome to learn-vue-app.</h1>
</div>`
      }
    }
  }
</script>

<style scoped>
.tutorial {
  width: 80%;
  margin: auto;
}
</style>
