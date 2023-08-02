<template>
<div class="btn">
  <slot></slot>
</div>
<!-- <h1 :class="$attrs.class" :style="$attrs.style">123</h1> -->
<h1 v-bind="$attrs">{{$attrs.title}}</h1>
</template>

<script>
export default {
  inheritAttrs: false, //속성상속
  created() { 
    console.log(this.$attrs);
  }
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