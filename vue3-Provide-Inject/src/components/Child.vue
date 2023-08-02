<template>
  <div>
    child : {{ msg }}
  </div>
</template>

<script>
export default {
  inject: [
    'msg'
  ]
}
</script>