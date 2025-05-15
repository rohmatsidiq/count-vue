<script setup>
import {ref} from 'vue'
const count = ref(0)
</script>

<template>
  <main>
    <h1>Conter</h1>
    <span id="value">{{ count }}</span>
    <div>
      <button @click="count--" id="decrease">-</button>
      <button @click="count++" id="increase">+</button>
    </div>
  </main>
</template>

<style scoped>

main {
  text-align: center;
}

#value {
  font-size: 50px
}

</style>