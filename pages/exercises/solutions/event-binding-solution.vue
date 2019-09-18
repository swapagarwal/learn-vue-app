<template>
  <div>
    <!-- You can ignore the structure of this .vue file for now. This will be covered in a later tutorial. -->

    <!-- Let's start by calling the "joke" method on this button's click. -->
    <button v-on:click="joke">Knock Knock!</button>
    <br>

    <!-- We have a counter and two buttons. Call their respective methods. -->
    Count: {{ count }}
    <button v-on:click="increment">Increase</button>
    <button v-on:click="decrement">Decrease</button>

    <!-- Mouse events can also act as triggers. Call the "foo" method on "mouseover" and "bar" method on "mouseout". -->
    <div v-bind:style="myStyle" v-on:mouseover="foo" v-on:mouseout="bar">Hover Over Me</div>

    <!-- We can also trigger events on key presses. Call "myEvent" on "keyup.enter". -->
    <input v-on:keyup.enter="myEvent" placeholder="Press the enter key...">
    <br>

    <!-- Refer the "shorthand" URL for an alternative syntax of v-on. Link that page here (remember the data-binding tutorial?). -->
    Bonus:
    <a :href="shorthand" target="_blank" rel="noopener noreferrer">Link</a>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        count: 0,
        myStyle: {
          fontWeight: 'bold',
          backgroundColor: '#90EE90'
        },
        shorthand: 'https://vuejs.org/v2/guide/syntax.html#v-on-Shorthand'
      }
    },
    methods: {
      joke() {
        alert('Who\'s there?');
      },
      increment() {
        this.count += 1;
      },
      decrement() {
        this.count -= 1;
      },
      foo() {
        this.myStyle.backgroundColor = '#FFB6C1';
      },
      bar() {
        this.myStyle.backgroundColor = '#90EE90';
      },
      myEvent() {
        alert('You pressed Enter!');
      }
    }
  }
</script>

<style scoped>

</style>
