<template>
  <h1>Home page..</h1>
  <h2>{{ wonMessage }}</h2>
</template>

<script>
export default {
  computed: {
    wonMessage() {
      return this.$store.state.won.message
    }
  }
}
</script>
