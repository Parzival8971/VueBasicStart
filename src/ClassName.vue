<template>
  <h1 
  v-bind:class="{ active: isActive }"
  v-on:click="activate">
  Hello?! ({{ isActive }})
</h1>
</template>

<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    activate() {
      this.isActive = true
      console.log(this.isActive)
    }
  }
}
</script>

<style scoped>
  .active {
    color: red;
    font-weight: bold;
  }
</style>