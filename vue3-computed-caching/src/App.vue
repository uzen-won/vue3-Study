<template>
  <h1 @click="add">{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
  <h1>{{ reversedMsg }}</h1>
</template>
 
<script>
export default {
  data() {
    return {
      //Getter Setter
      msg: 'Hello Computed!!'
    }
  },
  computed: {
    //Getter
    // reversedMsg() {  //caching이 되어있기 때문에 한번만 연산하고 출력한다. ///데이어 최적화
    //   return this.msg.split('').reverse().join('')
    // } 
    reversedMsg: {
      get() { 
        return this.msg.split('').reverse().join('')
      },
      set(NewValue) { 
        this.msg = NewValue
        console.log(NewValue)
      }
    }
  },
  methods: {  
    /* reverseMessage() { 
      return this.msg.split('').reverse().join('')
    }, */
    add() { 
      this.reversedMsg += "!?"
    }
  },
}
</script>