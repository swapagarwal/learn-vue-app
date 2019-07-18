<template>
  <div>
    <br><br>
    <span class="left">
      <nuxt-link v-if="previous($nuxt.$route.path)" :to="previous($nuxt.$route.path).path">{{previous($nuxt.$route.path).name}}</nuxt-link>
      <p v-else>&nbsp;</p>
    </span>
    <span class="center">
      <nuxt-link to="/">🏡 Home</nuxt-link>
    </span>
    <span class="right">
      <nuxt-link v-if="next($nuxt.$route.path)" :to="next($nuxt.$route.path).path">{{next($nuxt.$route.path).name}}</nuxt-link>
      <p v-else>&nbsp;</p>
    </span>
    <br><br>
  </div>
</template>

<script>
  import tutorial_data from '~/assets/tutorial-data.json'
  export default {
    tutorialData: tutorial_data,
    methods: {
      index: function(path) {
        return this.$options.tutorialData.findIndex(i => i.path == path);
      },
      name: function(path) {
        const currentIndex = this.index(path);
        return this.$options.tutorialData[currentIndex].name;
      },
      next: function(path) {
        const currentIndex = this.index(path);
        if (currentIndex < this.$options.tutorialData.length - 1) {
          return this.$options.tutorialData[currentIndex + 1];
        }
      },
      previous: function(path) {
        const currentIndex = this.index(path);
        if (currentIndex > 0) {
          return this.$options.tutorialData[currentIndex - 1];
        }
      }
    }
  }
</script>

<style scoped>
.left {
  float: left;
  width: 33%;
  text-align: center;
}
.center {
  float: left;
  width: 33%;
  text-align: center;
}
.right {
  float: left;
  width: 33%;
  text-align: center;
}
</style>
