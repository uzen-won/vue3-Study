<template>
 <Hello ref="hello"/>
</template>

<script>
import Hello from '~/components/Hello'
export default {
  //created에서는 사용 불가능
  mounted() { 
    // const h1El = document.querySelector('#hello')
    // console.log(h1El.textContent)
    console.log(this.$refs.hello.$refs)
  },
  components: {
    Hello
  }
}

</script>
