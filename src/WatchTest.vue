<template>
  <h1 v-on:click="changeMessage">{{ msg }}</h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() { 
    return {
      msg: 'Hello?'
    }
  },
  computed: {
    reversedMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  watch: {
    msg: function () {
      // data의 msg를 감시함, 바뀔때 실행
      console.log('msg:', this.msg)
    },
    reversedMessage() {
      // computed도 감시함
      console.log('reversedMessage', this.reversedMessage)
    }
  },
  methods: {
    changeMessage() {
      this.msg = 'Good!'
    }
  }
}
</script>

<style>

</style>