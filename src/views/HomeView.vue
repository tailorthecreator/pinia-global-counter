<script setup>
import { useCounterStore } from "@/stores/counter";

const storeCounter = useCounterStore()


</script>

<template>
  <div class="home"></div>
  <div class="count">{{ storeCounter.count }}</div>

  <div class="buttons">
    <button @click="storeCounter.decreaseCount">-</button>
    <button @click="storeCounter.increaseCount">+</button>
  </div>
  <hr>
  <div>
    This counter is: {{ storeCounter.oddOrEven }}
  </div>

</template>

<style>
.count {
  font-size: 60px;
  margin: 20px;
}

.buttons button {
  font-size: 40px;
  margin: 10px;
}
</style>