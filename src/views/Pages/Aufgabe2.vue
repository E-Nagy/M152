<template>

  <input type="text">

  <div>
      <button :class="bgColor + ' ' + textColor">{{textColor}} auf {{ bgColor }}</button>
  </div>

</template>

<script setup>

import { ref } from 'vue';

  const bgColor = ref('');
  const textColor = ref('');

</script>

<style>
div {
  width: auto;
  margin: auto;
  display: flex;
  justify-content: center;
  flex-direction: column;
 
}

input{
  margin-top: 20px;
  width: 20%;
  margin-left: auto;
  margin-right: auto;
}

button {
  border: none;
  border-radius: 5px;
  padding: 10px;
  font-weight: bold;
  font-size: medium;
  margin-top: 30px;
  margin-bottom: 30px;
}

h3 {
  margin-top: 20px;
  margin-bottom: 0;
}

 
</style>