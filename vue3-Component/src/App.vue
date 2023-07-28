<template>
  <MyBtn>Banana</MyBtn>
  <MyBtn :color="color">Apple</MyBtn>
  <MyBtn Large color="red">Cherry</MyBtn>
  <MyBtn />
</template>

<script>
import MyBtn from '~/components/MyBtn'

export default {
  data() { 
    return {
      color: '#000'
    }
    
  },
  components: {
    MyBtn
  }
}
</script>
