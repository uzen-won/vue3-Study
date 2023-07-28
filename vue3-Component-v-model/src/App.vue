<template>
  <!-- 

    @change 
    v-model.lazy=""   
    -> 입력 완료되면 값 갱신

    v-model.number=""
    -> 사용자에게 숫자열 입력받아야 될때

   -->
  <h1>{{ msg }}</h1>
  <input type="text" v-model="msg">
</template>

<script>
export default {
  data() { 
    return {
      msg : 'Hello World!!'
    }
  },
  watch: { 
  msg(){ 
    console.log(this.msg.trim())
  }
  }
}
</script>
<style scoped lang="scss">
input[type="text"] {
  margin: 10px;
  font-size: 32px;
  line-height: 60px;
  padding: 0 10px;
  width: 400px;
  box-sizing: border-box;
}
</style>
