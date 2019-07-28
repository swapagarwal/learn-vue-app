<template>
  <div class="tutorial">
    In simple terms, data binding refers to the ability of views to automatically update when models (data) change.
    <br><br>
    You can use the "v-bind" attribute to attach data to an element. The syntax is:
    <pre v-highlightjs="syntax"><code class="html"></code></pre>
    <br>
    For example, we can add a class to an element like this:
    <pre v-highlightjs="example"><code class="html"></code></pre>
    <br>
    Let's assign a value to the "className" variable and define the style for "color-red" class.
    <pre v-highlightjs="assign"><code class="html"></code></pre>
    <br>
    And we get the heading text, styled in red color, as follows:
    <h1 v-bind:class="className">Hello World</h1>
    <br>
    Try out the exercise below. It will help you reinforce some previous concepts as well. If you get stuck, feel free to refer to the solution file.
    <br><br>
    <Exercise/>
    When you're done, move on to the next tutorial.
    <br><br>
    P.S. Since it's a common use-case, Vue provides a shorthand for this directive. Apart from the v-bind:attribute="expression" syntax, we can use :attribute="expression" as well.
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
        className: 'color-red',
        syntax: `v-bind:attribute="expression"`,
        example: `<h1 v-bind:class="className">Hello World</h1>`,
        assign: `<script>
    export default {
        data() {
            return {
                className: 'color-red'
            }
        }
    }
<\/script>
<style scoped>
.color-red {
    color: red;
}
<\/style>`
      }
    }
  }
</script>

<style scoped>
.color-red {
  color: red;
}
.tutorial {
  width: 80%;
  margin: auto;
}
</style>
