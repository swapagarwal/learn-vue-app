<template>
  <div>
    <span class="left">
      <p>This is your goal.</p>
      <p>Location: {{solution($nuxt.$route.path).display}}</p>
      <iframe width="80%" :src="solution($nuxt.$route.path).source"/>
    </span>
    <span class="right">
      <p>Your code goes here.</p>
      <p>Location: {{exercise($nuxt.$route.path).display}}</p>
      <iframe width="80%" :src="exercise($nuxt.$route.path).source"/>
    </span>
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
      exercise: function(path) {
        const currentIndex = this.index(path);
        return this.$options.tutorialData[currentIndex].exercise;
      },
      solution: function(path) {
        const currentIndex = this.index(path);
        return this.$options.tutorialData[currentIndex].solution;
      }
    }
  }
</script>

<style scoped>
.left {
  float: left;
  width: 50%;
  text-align: center;
}
.right {
  float: left;
  width: 50%;
  text-align: center;
}
</style>
