<template>
  <div class="btn">
    <slot></slot>
  </div>
  <h1 @dblclick="$emit('user',$event)">A</h1>
  <!-- emit이라는 옵션을 통해서()안에 있는 이벤트를 사용한다 -->
  <input type="text" v-model="msg">
</template>

<script>
export default {
  inheritAttrs: false,
  emits: [ 
    'user', //click 이라는 이벤트를 사용할것을 정의
    'changeMsg'
  ],
  data() {
    return {
      msg : ''
    }
  },
  watch: {
    msg() { 
      this.$emit('changeMsg', this.msg)
    }
  },
  methods: {
  },
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