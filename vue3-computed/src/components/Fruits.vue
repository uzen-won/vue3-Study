<template>
  <section v-if="hasFruits">
    <h1>Fruits</h1>
    <ul>
      <li
        v-for="fruit in fruits"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
  <section>
    <h1>reverseFruits</h1>
    <ul>
      <li
        v-for="fruit in reverseFruit"
        :key="fruit">
        {{ fruit }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits: [
        'Apple',
        'Banana',
        'Cherry'
      ]
    }
  },
  computed: { //옵션
    hasFruits() { //매소드
      return this.fruits.length > 0
    },
    reverseFruit() {
      return this.fruits.map((i) => { 
        return i.split('').reverse().join('')
      })
    }


  }
}
</script>
