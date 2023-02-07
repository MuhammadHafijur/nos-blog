<template>
  <div class="home">
    <h1>Home</h1>
    <h1>Refs</h1>
    <p>{{ ninjaOne.name }} - {{ ninjaOne.age }}</p>
    <button @click="updateNinjaOne">update ninja one</button>
    <button @click="updateNinjaTwo">update ninja one</button>
    <h2>Reactive</h2>
    <p>{{ ninjaTwo.name }} - {{ ninjaTwo.age }}</p>
  </div>
</template>

<script>
import { ref, reactive } from 'vue'



export default {
  name: 'Home',
  setup(){

    const ninjaOne = ref({ name: 'mario', age: 30})
    const ninjaTwo = reactive({ name: 'rahim', age: 35})

    const updateNinjaOne = () => {
      ninjaOne.value.age = 40
    }

    const updateNinjaTwo = () => {
      ninjaTwo.age = 45
    }

    return { ninjaOne, updateNinjaOne, updateNinjaTwo, ninjaTwo}
  }
}
</script>
