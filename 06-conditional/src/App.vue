<script setup>
import { ref, computed } from 'vue';
const isLogin = ref(true);

//toggle login là 1 function
const togglelogin = () => {
  isLogin.value = !isLogin.value
}

const invisible = ref(true)
const changeinvisible = () => {
  invisible.value = !invisible.value
}

const status = ref('chào')
const changeStatus = () => {
  if (status.value === 'chào') {
    status.value = 'tạm biệt'
  } else {
    status.value = 'chào'
  }
}
</script>

<template>
  <div>
        <h1 v-if="isLogin">Xin chào</h1>
        <h1 v-else>Xin lỗi</h1>
      <h1 v-show="invisible">Hello</h1>
    <button @click = "togglelogin">Toggle Login</button>
    <br>
    <h1 v-if="status === 'chào'">Xin chào</h1>
    <h1 v-else>tạm biệt</h1>
    <button @click = "changeStatus">Change Status</button>
    <button @click = "changeinvisible">{{ invisible ? 'hide' : 'show' }}</button>
  </div>
</template>