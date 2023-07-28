<template>
  <div class="btn" :style="{backgroundColor:color}">
    Apple
  </div>

</template>  

<script>
export default {
  props: {
    color: {
      type: String,
      default: 'gray'
    },
    fontSize: {
      type: String,
      default: '20px'
    },
    Large: {
      type: String,
      default : ""
    }
  }
}
</script>

<style scoped>
 .btn {
  display: inline-block;
  margin: 4px;
  padding: 6px 12px;
  border-radius: 4px;
  background-color: gray;
  color: #fff;
  cursor: pointer;
 }
</style>