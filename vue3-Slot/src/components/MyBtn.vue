<template>
  <div class="btn">
    <slot name="icon">Apple</slot>
    <slot name="text">Apple</slot>
  </div>
</template>

<script>
export default {
  
}
</script>

<style scoped lang="scss">
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