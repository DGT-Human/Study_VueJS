<script setup>
import { nextTick, reactive, computed , ref} from 'vue'

// const auth = reactive({
//   name: 'Book 1',
//   chapters: []
// })
//
// const addChapter = () => {
//   auth.chapters.push('Chapter')
// }
//
// const isPublished = () => {
//   return auth.chapters.length > 0 ? 'Có' : 'Không'
// }


// const isPublished = computed(() => {
//   return auth.chapters.length > 0 ? 'Có' : 'Không'
// }) //computed giúp tính toán giá trị mà không cần gọi hàm. chỉ tính lại khi giá trị thay đổi


const firstname = ref('Du Gia')
const lastname = ref('A')

const fullname = computed ({//computed giúp tính toán giá trị mà không cần gọi hàm. chỉ tính lại khi giá trị thay đổi
  get(){ //lấy giá trị mà không cần gọi hàm
    return firstname.value + ' ' + lastname.value //nối chuỗi
  },
  set(value){ // set giá trị cho computed
    [firstname.value, lastname.value] = value.split(',') //tách chuỗi thành mảng
  }
})
const changeFullname = () => {
  fullname.value = 'Du Gia,Tien'
}
</script>

<template>
  <div>
<!--    <p id="count">Book name: {{ auth.name }}</p>-->
<!--    <p id="count">Đã xuất bản: {{ isPublished() }}</p>-->
<!--    <button @click = "addChapter">Add chapter</button>-->

    <p id="count">Fullname: {{ fullname }}</p>
    <p id="count">First Name: {{ firstname }}</p>
    <p id="count">Last Name: {{ lastname }}</p>
    <button @click="changeFullname">Change</button>
  </div>
</template>


