<template>
  <div class="btn" :style="{backgroundColor:color}" :class="{Large}">
    <slot></slot> <!-- 컴포넌트의 열리고 닫힌태그 사이에 들어가는 데이터를 slot 안에서 출력 -->
  </div>

</template>  

<script>
export default {

  props: {
    color: {
      type: String,
      default: 'gray'
    },
    Large: {
      type: Boolean,
      default: false,
    },
    text: {
      type: String,
      default:''
    }
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
  &.Large {
    font-size: 20px;
    padding: 10px 20px;
  }
 }
</style>