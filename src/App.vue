<script setup>
import { useCounterStore } from "@/stores/useCounterStore";
const counterStore = useCounterStore();
</script>

<template>
  <h1>Приветики!</h1>
  <hr />
  <button @click="counterStore.increment">+</button>
  итого: {{ counterStore.count }}
  <button @click="counterStore.unIncrement">-</button>
</template>

<style scoped></style>
























<!-- isPalindrome(value) {

  const checkValue = value.replace(/\s/g, '').toLowerCase();
  return checkValue === checkValue.split('').reverse().join('')

}; -->
