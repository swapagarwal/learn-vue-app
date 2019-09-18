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
    <br><br>
    Try out the exercise below. It will help you reinforce some previous concepts as well. If you get stuck, feel free to refer to the solution file.
    <br><br>
    <Exercise/>
    Refresh the page to see the changes reflected above. When you're done, move on to the next tutorial.
    <br><br>
    P.S. Being a common use-case (interactivity is everywhere), Vue provides a shorthand for this directive as well. We can replace v-on:event.modifier="expression" with @event.modifier="expression".
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
