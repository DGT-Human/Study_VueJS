<script setup>
// khai bao bien
const message = 'Hello Vue 3'
const rawHtml = '<div><h1>title</h1><span style="color: red">This should be red.</span></div>'
const buttonID = 'button-id'
const buttonClass = 'btn btn-primary'
const isButtonDisabled = false
const objectOfAttrs = {
  id: 'container',
  class: 'wrapper',
  style: {
    color: 'red',
    fontSize: '20px'
  }
}
const number = 0
const listString = 'a,b,c,d,e,f,g,h,i,j'
const convertTold = (data) => data.split(',').reverse().join('-') //reverse la dao nguoc chuoi
const attributeName = 'href'
const url = 'https://google.com'



function sayHello(){
  alert('Hello')
}

</script>

<template>
  <h1>Syntax</h1>
  <p>Message: {{ message }}</p>
  <span v-html="rawHtml"></span>
<!--  // v-bind la cach khai bao thuoc tinh-->
  <button v-bind:id="buttonID" :class="buttonClass" :disabled="isButtonDisabled">{{ isButtonDisabled ? 'Disabled' : 'Click here' }}</button>
  <button :id="buttonID" :class="buttonClass" >Click</button>
  <button v-bind="objectOfAttrs" > Click here!!</button>
  <button :id = "convertTold(listString)">Number: {{ number * 2 }}</button>
<!--Đối Số Động-->
  <a v-bind:[attributeName]="url">Click</a>
<!--Gọi hàm-->
  <a v-on:click="sayHello"> Click </a>

  <!-- cách viết tắt -->
<!--  <a @[attributeName]="url"> Click </a>-->



</template>


