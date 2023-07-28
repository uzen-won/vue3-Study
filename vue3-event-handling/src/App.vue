<template>
  <!-- 
    인수와 이벤트 객체 둘 다 사용하려면
    @click="NAME('인수', $이벤트객체)"
    $를 붙여주는게 VUE js 문법
   -->
  <!-- <button @click="handler('hi', $event)">
    CLick 1!
  </button>
  
  <br><br>
  <button @click="handler('what', $event)">
    CLick 2!!
  </button> -->

  <!-- 여러개의 함수 동시에 실행 -->
  <!-- 매소드 뒤에 소괄호 붙여야 실행됨 -->
  <button @click="handlerA(), handlerB() ,handlerC()">
    Click!
  </button>
</template>

<script>
export default {
  data() {
    return {

    }
  },
  methods: {
    // handler(e, event) {
    //   console.log(e)
    //   console.log(event)

    // }

    handlerA() { 
      console.log('A')
    },
     handlerB() {
      console.log('B')
     },
     handlerC() {
      console.log('C')
    }
  }

}
</script>
