<template>
  <!-- 
    1. 양방향 바인딩
    데이터와 화면에 출력되는 값을 일치 시킨다
    둘중 하나가 바귀면 같이 바뀜

    html
    @input="데이터 = $event.target.value"
    methods
    this.데이터 = e.target.value

    v-model="데이터"를 활용하면 편리하게 구현 가능

    ※한글을 v-model로 구현하면 한박자 느리게 완성됨
      한글은 단방향에서 연결해줘야함
   -->
  <h1>{{ msg }}</h1>
  <!-- <input type="text" :value="msg" @input="msg = $event.target.value"> -->
  <input type="text" v-model="msg">
  <h1>{{ checked }}</h1>
  <input type="checkbox" v-model="checked">
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      checked: false
    }
  },
  methods: {
    // handler(e) { 
    //   console.log(e.target.value);
    //   this.msg = e.target.value
    // }
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