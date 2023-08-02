<template>
  <MyBtn>
    <!-- 
      slot안에 있는 요소 순서 정하기
      # = :v-slot
      slot의 name이라는 속성을 이용해서 순서 지정
    -->

    <template #text><span>Banana</span></template>
    <template #icon><span>(B)</span></template>

    
    
    
  </MyBtn>
    
</template>
<script>
import MyBtn from '~/components/MyBtn'
export default {
  data() { 

  },
  components: {
    MyBtn
  }
}
</script>
