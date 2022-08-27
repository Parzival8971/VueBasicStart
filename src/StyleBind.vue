<template>
  <h1 
  v-bind:style="{ color: color, fontSize: fontSize}"
  v-on:click="changeStyle"
  >Hello
  </h1>
  <h1 
  v-bind:style="[fontStyle, backgroundStyle]"
  v-on:click="changeStyle"
  >Hello2
  </h1>
</template>

<script>
export default {
  data() {
    return {
      fontStyle: {
        color: 'blue',
        fontSize: '100px'
      },
      backgroundStyle: {
        backgroundColor: 'black'
      },
      color: 'orange',
      fontSize: '30px'
    }
  },
  methods: {
    changeStyle() {
      this.color = 'red'
      this.fontSize = "50px"
      this.fontStyle.color = '#234234'
      this.fontStyle.fontSize = "40px"
    }
  }
}
</script>

<style>

</style>