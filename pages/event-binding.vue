<template>
  <div class="tutorial">
    Often we need to execute some JavaScript code when an event (clicking a HTML element, submitting a form, pressing a key, etc.) occurs.
    <br><br>
    Vue provides the "v-on" directive for this use-case. The syntax is:
    <pre v-highlightjs="syntax"><code class="html"></code></pre>
    <br>
    Let's try to show a popup when a button is clicked. To do that, we can add the event handler like this:
    <pre v-highlightjs="example"><code class="html"></code></pre>
    <br>
    Now, we have to define the "showPopup" method.
    <pre v-highlightjs="define"><code class="html"></code></pre>
    <br>
    That's all! Test out the button by clicking it:
    <button v-on:click="showPopup">Click Me</button>
    <TutorialNavigation/>
  </div>
</template>

<script>
  import TutorialNavigation from '~/components/TutorialNavigation.vue'
  export default {
    components: {
      TutorialNavigation
    },
    data() {
      return {
        syntax: `v-on:event.modifier="expression"`,
        example: `<button v-on:click="showPopup">Click Me</button>`,
        define: `<script>
    export default {
        methods: {
            showPopup() {
                alert('It works!');
            }
        }
    }
<\/script>`,
      }
    },
    methods: {
      showPopup() {
        alert('It works!');
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
