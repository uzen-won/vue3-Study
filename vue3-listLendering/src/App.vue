<template>
  <ul>
    <li v-for="fruit in newFruits" :key="newFruits.id">
      {{ fruit.name }}
    </li>
  </ul>
</template>

<script>
export default {
  data() { 
    return {
      fruits: ['Apple', 'Banana', 'Cherry']
    }
  },
  computed: {
    newFruits() { 
      return this.fruits.map((fruit,i) => { 
        return {
          id: i,
          name : fruit
        }
      })
    }
   }
}
</script>
