<script setup>
import { ref, computed } from 'vue';
// const isActive = ref(true);
// const hasError = ref(false);
//
// const classObject = computed(() => ({
//   active: isActive.value,
//   'has-error': hasError.value
// }));
//
// const change = () => {
//   isActive.value = !isActive.value;
// }

const color = ref('red');
const backgroundColor = ref('blue');
const fontSize = ref('30px');
</script>

<template>
  <div>
<!--    // co class active khi isActive = true-->
<!--    <button class="button" :class="classObject" @click="change">{{ isActive ? 'Active' : 'Inactive'}}</button>-->
<!--    <button class="button" :class="{ active: isActive, 'has-error': hasError }" @click="change">{{ isActive ? 'Active' : 'Inactive'}}</button>-->
<!--    <button class="button" :class="[isActive ? 'active':'', {'has-error':hasError}]" @click="change">{{ isActive ? 'Active' : 'Inactive'}}</button>-->
    <button :style=" {backgroundColor, color, fontSize}">hello</button>
  </div>
</template>

<!--<style>-->
<!--.button{-->
<!--  border: none;-->
<!--  background: #0e8c8c;-->
<!--  color: #0d71bb;-->
<!--  padding: 10px 20px;-->
<!--  border-radius: 5px;-->
<!--  cursor: pointer;-->
<!--  &:hover {-->
<!--    background: #0e6eb8;-->
<!--    color: #0d71bb;-->
<!--  }-->
<!--}-->
<!--.active {-->
<!--  background: #88bb55;-->
<!--  color: #ededf3;-->
<!--  &:hover {-->
<!--    background: #8d9e13;-->
<!--  }-->
<!--}-->

<!--.has-error {-->
<!--  background: #ee4266;-->
<!--  color: #e26e70;-->

<!--  &:hover {-->
<!--    background: #e4606d;-->
<!--  }-->
<!--}-->

<!--</style>-->
