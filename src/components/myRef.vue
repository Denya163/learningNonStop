<script setup>
import { ref, onMounted } from "vue";

const count = ref(0); // Создаем реактивную переменную

const increment = () => {
  count.value++; // Меняем значение через .value
};

const inputRef = ref(null);

onMounted(() => {
  inputRef.value.focus(); // Автоматически ставим фокус на поле ввода
});

const boxRef = ref(null);

const changeColor = () => {
  boxRef.value.style.backgroundColor = 'lightblue';
};

function hiDebounce() {alert('hi')};
hiDebounce = _.debounce(hiDebounce, 2000);

</script>



<template>
  <input ref="inputRef" type="text" placeholder="Введите текст" />

  <button @click="increment">Count: {{ count }}</button>
  <button @click="hiDebounce">Count: {{ count }}</button>

  <div ref="boxRef" class="box">Здесь меняется цвет</div>
  <button @click="changeColor">Изменить цвет</button>
</template>



<style>
.box {
  width: 100px;
  height: 100px;
  background-color: lightgray;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>