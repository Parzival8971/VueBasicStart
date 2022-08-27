<template>
  <h1 v-on:click="add">1: {{ text }}</h1>
  <h1 v-once v-on:click="add2">2: {{ text }}</h1>
  <h1 v-html="text3"></h1>
  <h1>4: {{ text3 }}</h1>
  <h1 v-bind:class="text4">5: {{ text4 }}</h1>
  <h1 v-bind:[attr]="'active'" v-on:[event]='add'>6: {{ text4 }}</h1>
</template>

<script>
export default {
  data() {
    return {
      text: 'Hellow World!',
      text2: 'V-once Test',
      text3: '<div style="color: red">v-html Code</div>',
      text4: 'active',
      attr: 'class',
      event: 'click'
    }
  },
  methods: {
    add() {
      this.text4 += '!'
    },
    add2() {
      this.text2 += '!'
    }
  }
}
</script>

<style scoped>
  .active {
    color: royalblue;
    font-size: 100px;
  }
</style>