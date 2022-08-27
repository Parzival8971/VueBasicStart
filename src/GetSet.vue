<template>
  <button v-on:click="add">ADD</button>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reverseMessage() }}</h1>
</template>

<script>
// import FruitsTest from './components/FruitsTest.vue'

export default {
  components: {
    // FruitsTest : FruitsTest
  },
  data() {
    return {
      // Getter 값을 얻어내는 용도로도 사용하고, Setter 값을 지정하는 용도로도 사용한다.
      msg: "Hellow Computed!"
    }
  },
  computed: {
    // 미리 캐싱 됨
    // 읽기전용임(Readonly)
    // 값을 얻어내는 형식으로만 사용함 Getter
    // reversedMessage() {
    //   return this.msg.split('').reverse().join('')
    // },
    reversedMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(value) {
        this.msg = value 
        console.log(value)
      }
    }
  },
  methods: {
    // 실행할 때마다 리랜더링 됨
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    },
    add() {
      this.reversedMessage += '1?'
      // this.msg += '1?'
    }
  }
}
</script>

<style>

</style>