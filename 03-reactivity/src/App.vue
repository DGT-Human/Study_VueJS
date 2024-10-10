<script setup>
import { nextTick,ref } from 'vue'
// import { reactive } from 'vue' //reactive giống như ref nhưng cho object
//
// export default {
//   // `setup` là một hook đặc biệt dành cho Composition API.
//   setup() {
//     const count = ref(0)
//
//     // export ref cho mẫu
//     return {
//       count
//     }
//   }
// }
// const object = reactive({
//   count: 2,
//   user: {
//     age: 20
//   },
//   array: [1,2,3]
// })

// const change = () => {
//   // object.value.count++
//   // object.value.user.age++
//   // object.value.array.push(4)
//   object.count++
//   object.user.age++
//   object.array.push(4)
// }
const count = ref(0)
// count.value++
const increment = async() => { //async để chờ nextTick
  count.value++
  console.log(document.getElementById('count').innerText)
  await nextTick() //chờ đến khi DOM được cập nhật
  console.log(document.getElementById('count').innerText)
}
</script>

<template>
<div>
  <h1 id = "count"> Count: {{ count }}</h1>
<!--  <h1> Count: {{ object.count }}</h1>-->
<!--  <h1> age: {{ object.user.age }}</h1>-->
<!--  <h1> age: {{ object.array }}</h1>-->
<!--  <button v-on:click="increment">Increment</button>-->
<!--  <button @click="change">Change</button>-->
  <button @click="increment">Change</button>
</div>
</template>


