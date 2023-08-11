<template>
  <span>{{ asd }}</span>
  <ul>
    <li v-for="li in list" :key="li.id">{{ li.id }} : {{li.name}}</li>
  </ul>
  <p>{{inputTxt}}</p>
  <input 
  type="text" 
  :value="inputTxt" 
  @change="inputTxt = $event.target.value"
  @keydown="showEvent">
</template>
<script>
export default {
  data() {
    return {
      asd: '123',
      list: [
        { id: 0, name: '000' },
        { id: 0, name: '111' },
        { id: 0, name: '222' },
        { id: 0, name: '333' },
      ],
      inputTxt: 'why',
    }
  },
  watch: {
    inputTxt() {
      console.log(this.inputTxt)
    }
  },
  computed: {
    
   },
  methods: {
    showEvent(event) { 
      console.log(event)
    }
  }
}
</script>
