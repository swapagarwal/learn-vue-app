<template>
  <div>
    <!-- You can ignore the structure of this .vue file for now. This will be covered in a later tutorial. -->

    <!-- Use the double braces syntax to render the "name" here. -->
    Name: TODO
    <br>

    <!-- Use the double braces syntax to render the sum of "a" and "b". -->
    2 + 3 = TODO
    <br>

    <!-- Use the v-bind syntax to link to the "guide" here. -->
    Here's the official documentation of Vue.js:
    <a href="#" target="_blank" rel="noopener noreferrer">Link</a>

    <!-- Use the v-bind syntax to add the "style" classes to the div. -->
    <div>
      This text should be bold and underlined.
    </div>

    <!-- Refer the "shorthand" URL and use it here to link to that page. -->
    Bonus:
    <a href="#" target="_blank" rel="noopener noreferrer">Link</a>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        name: 'Jane Doe',
        a: 2,
        b: 3,
        guide: 'https://vuejs.org/v2/guide/',
        shorthand: 'https://vuejs.org/v2/guide/syntax.html#v-bind-Shorthand',
        style: ['bold', 'underline']
      }
    }
  }
</script>

<style scoped>
.bold {
  font-weight: bold;
}
.underline {
  text-decoration: underline;
}
</style>
