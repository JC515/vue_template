<script setup>
import {ref} from 'vue'

const name = ref('yjc')
const btnFunc1 = () => {
  if (name.value === 'yjc') {
    name.value = '杨佳成'
  } else {
    name.value = 'yjc'
  }
  //点击一次后，1秒内不能再点击
  document.querySelector('#nameBtn').disabled = true
  //1秒后恢复
  setTimeout(() => {
    document.querySelector('#nameBtn').disabled = false
  }, 1000)
}

const fruits = ref(['apple', 'banana', 'orange', 'grape']);
</script>

<template>
  <p>Page4Test</p>
  <form>
    <label>Name:</label>
    <input v-model="name">
    <button type="button" @click="btnFunc1" style="font-size: 20px" id="nameBtn">button</button>
    <hr>
    <div style="background-color: aliceblue;">
      <ul>
        <li v-for="(fruit , index) in fruits" :key="index">{{ index + 1 }}.{{ fruit }}</li>
      </ul>
    </div>
  </form>
</template>

<style scoped>
ul {
  padding: 0;
  margin: 30px;
  display: inline-flex;
  flex-wrap: nowrap;
  flex-direction: column; 
  gap: 16px 0;
}

li {
  width: max-content;
  padding: 16px;
  border-radius: 4px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.25s ease-in-out;
}

li:hover {
  transform: translateY(-4px);
}
</style>