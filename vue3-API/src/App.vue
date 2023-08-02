<template>
  <div @click="increase">
    {{count}}
  </div>
</template>

<script>
export default {
  data() { 
    return {
      count: 0
    }
  },
  methods: {
    increase() { 
      this.count +=1
    }
  }
}
</script>

