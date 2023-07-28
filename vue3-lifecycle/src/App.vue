<template>
  <h1><span>count : </span>{{ count }}</h1>
</template>

<script>
export default {
  data() {
    return {
      count: 2
    } 
  },
  beforeCreate() { //컴포넌트가 생성되기 직전에  // 활용도 없음
    console.log('BeforeCreate!', this.count) //BeforeCreate! undefined
  },
  created() {  // 컴포넌트 작성되고 나서   // 많이 사용됨 
    console.log('Created!', this.count) //Create! 2
  },
  beforeMount() {  // html에 컴포넌트가 연결이 되기 전  // 활용도 떨어짐
    console.log('BeforeMount!')
    console.log(document.querySelector('h1')) // Null

  },
  mounted() { //화면에 컴포넌트가 출력 되고 나서  // 많이 사용됨
    console.log('Mounted!')
    console.log(document.querySelector('h1')) // <h1>2</h1>
  },
}
</script>

<style lang="scss">
h1 {
  color: royalblue;
  font-size: 40px;
  span {
    color: green;
  }
}
</style>