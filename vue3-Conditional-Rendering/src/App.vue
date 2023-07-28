<template>
  <button @click="active">
    click
  </button>
  <!-- 
    v-if -> 랜더링 X
    v-show -> 랜더링 O
   -->
  <h1 v-if="con">Hello?!</h1> 
  <h1 v-show="con">HELLO?!</h1>
   <!-- template html에 랜더링 X -->
  <!-- <template v-if="con">
    <h1>Title</h1>
    <p>paragraph1</p>
    <p>paragraph2</p>
    <p>paragraph3</p>
  </template> -->
</template>

<script>
export default {
  data() { 
    return {
      con: false,
    }
  },
  methods: {
    active() { 
      this.con = !this.con
    } 
  }
}
</script>
