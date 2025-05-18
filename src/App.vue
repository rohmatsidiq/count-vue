<!-- <script setup> -->
<script>
import { ref } from "vue";

export default {
  // options api =========================
  // buat variable
  // data() {
  //   return {
  //     count: 0,
  //   };
  // },
  // // buat fungsi
  // methods: {
  //   increase() {
  //     this.count++;
  //   },
  //   decrease() {
  //     this.count--;
  //   },
  // },

  // compositon api ==========================
  setup() {
    const count = ref(0);
    function increase() {
      count.value++;
    }
    function decrease() {
      count.value--;
    }
    return {
      count,
      increase,
      decrease,
    };
  },
};
</script>

<template>
  <main>
    <h1>Conter</h1>
    <span id="value">{{ count }}</span>
    <div>
      <button @click="decrease" id="decrease">-</button>
      <button @click="increase" id="increase">+</button>
    </div>
  </main>
</template>

<style scoped>
main {
  text-align: center;
}

#value {
  font-size: 50px;
}
</style>
