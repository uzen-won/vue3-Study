<template>
  <!--
    1. 수식어
    @click.prevent -> 기본동작 막기
    @click.once -> 매소드 한번만 실행
    @click.prevent.once -> 체이닝 가능
  -->

  <!-- 
    2. 이벤트 버블링
    자식 요소에 이벤트가 걸려있을때 
    부모 요소로 이벤트가 타고 올라가는것

    - 이벤트 버블링 방지
    event (e){
      e.stopPropagation();
    }
    @click.stop
   -->

  <!-- 
    3. 이벤트 캡처링
    부모요소에 있는 이벤트가 자식요소로 타고 내려가는것
    @click.capture
    -->

  <!-- 
    4. 정확하게 영역 지정
    클릭하는 영역만을 정확하게 클릭해야 동장
    @click.self
     -->

  <!-- 
    5. @wheel 마우스 휠 이벤트
    @wheel.passive
    화면의 스크롤과 로직 처리를 분리해서 사용환경을 쾌적히게
  -->

  <!-- 
    6. 키다운 이벤트
    @keydown.enter -> enter를 눌렀을 때만 작동
    체이닝 가능
     @keydown.ctrl.enter -> ctrl + enter
     @keydown.ctrl.shift.enter -> ctrl + shift + enter

   -->

  <input type="text" @keydown.ctrl.enter="handler">
  <div class="result"></div>
</template>

<script>
export default {
  data() {
    return {

    }

  },
  methods: {
    handler() {
      console.log('ENTER!!')
    },

    /* handlerA(e) {
      this.abc += '!'
      // console.log(e.target) //target -> 실제로 클릭이 된 요소
      // console.log(e.currentTarget) //currentTarget -> current 타켓이 실행된 이벤트가 걸려있는 요소
      //console.log(this.abc)
      console.log(e)
    }, */

  },
}
</script>

<style scoped lang="scss">
.parent {
  cursor: pointer;
  width: 200px;
  height: 100px;
  background-color: royalblue;
  margin: 10px;
  padding: 10px;
  overflow: auto;

  .child {
    cursor: pointer;
    width: 100px;
    height: 2000px;
    background: linear-gradient(to Bottom, orange, rgb(249, 58, 0));
  }
}
</style>