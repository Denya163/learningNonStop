<script setup>
import { ref } from "vue";

const count = ref(0); // Создаем реактивную переменную

const increment = () => {
  count.value++; // Меняем значение через .value
};
</script>

<template>
  <button @click="increment">Count: {{ count }}</button>
</template>