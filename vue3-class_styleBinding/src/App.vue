<template>
  <h1
    :style="[fontStyle, backgroundStyle]"
    @click="changeStyle">
    hello?!
     
  </h1>
</template>

<script>

export default {
  data() { 
    return {
      // color: 'orange',
      // fontSize : '30px'
      fontStyle: {
        color: 'orange',
        fontSize: '30px'
      },
      backgroundStyle: {
        backgroundColor : "black"
      } 
    }
  },
  methods: { 
    changeStyle() { 
      this.fontStyle.color = 'red'
      this.fontStyle.fontSize = "50px"
    },
  }
}

</script>