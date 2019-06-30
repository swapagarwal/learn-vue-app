<template>
  <div>
    <h1 :class="className">Hello World</h1>
    <button :title="title">Hover Over Me</button>
    <button :class=" { 'is-loading': isLoading } " @click="toggleIsLoading">Click Me</button>

    data-binding
    v-bind:attribute="expression"
    eg: v-bind:class="['foo', 'bar']"
    :

    v-on:event.modifier="expression"
    eg: v-bind:keypress.shift.ctrl.a="selectAll"
    @

    v-bind:value="value"
    v-on:change="event => value = event.target.value"
    ===
    v-model="value"
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
        className: 'color-red',
        title: 'Now the title is being set via JavaScript.',
        isLoading: false
      }
    },
    methods: {
      toggleIsLoading() {
        this.isLoading = ! this.isLoading;
      }
    }
  }
</script>

<style scoped>
.color-red {
  color: red;
}
.is-loading {
  background: red;
}
</style>
