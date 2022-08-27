<template>
  <!-- <button v-on:click="handler">Click Me!</button>
  <h1 v-if="isShow">Hello?</h1>
  <h1 v-else-if="count > 3">
    Count > 3
  </h1>
  <h1 v-else>Good!</h1> -->
  
  <button v-on:click="handler">Click Me!</button>
  <template v-if="isShow">
    <h1>Title</h1>
    <p>Pargagraph 1</p>
    <p>Pargagraph 2</p>
  </template>
</template>

<script>
export default {
  data() {
    return {
      isShow: true,
      count: 0
    }
  },
  methods: {
    handler() {
      this.isShow = !this.isShow
      this.count += 1
    }
  }
}
</script>

<style>

</style>