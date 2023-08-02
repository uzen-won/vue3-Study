<template>
  <Child/> <!-- app.vue에서 받아온 props를 다시 Child에 내려준다 -->
</template>

<script>
import Child from "~/components/Child"

export default {
  components: { 
    Child
  },
}  
</script>