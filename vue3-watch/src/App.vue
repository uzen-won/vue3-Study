<template>
  <h1 @click="changeMsg">{{ msg }}</h1>
  <h1>{{ reverseMsg }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: 'Hello?',
    }
  },
  computed: {
    reverseMsg() {
      return this.msg.split('').reverse().join('')
    }
    // reverseMsg: {
    //   get() { 
    //     return this.msg.split('').reverse().join('')
    //   },
    //   set(v) { 
    //     this.msg = v
    //   }
    // }
  },
  watch: {
    // msg () { 
    //   console.log(`msg: ${this.msg}`)
    // },
    reverseMsg() {
      console.log(`reverseMsg: ${this.reverseMsg}`)
    },
    msg(New) {
      console.log(`msg: ${New}`)
    }
  },
  methods: {
    changeMsg() {
      this.msg = 'Good!'
    }
  }

}
</script> 