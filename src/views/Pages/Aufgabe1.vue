<template>

    <div>
        <button :class="bgColor + ' ' + textColor">{{textColor}} auf {{ bgColor }}</button>

        <h3>Hintergrund</h3>
        <ul>
            <li @click="bgColor = 'bg-green'">
                Grün 
            </li>
            <li @click="bgColor = 'bg-gold'">
                Gold 
            </li>
            <li @click="bgColor = 'bg-darkblue'">
                Dunkelblau 
            </li>
            <li @click="bgColor = 'bg-red'">
                Rot 
            </li>
            <li @click="bgColor = 'bg-purple'">
                Lila 
            </li>
        </ul>

        <h3>Text</h3>
        <ul>
            <li @click="textColor = 'text-green'">
                Grün 
            </li>
            <li @click="textColor = 'text-gold'">
                Gold 
            </li>
            <li @click="textColor = 'text-darkblue'">
                Dunkelblau 
            </li>
            <li @click="textColor = 'text-red'">
                Rot
            </li>
            <li @click="textColor = 'text-purple'">
                Lila
            </li>
        </ul>
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

.bg-green{
    background-color: rgb(40, 91, 40);
}
.bg-gold{
  background-color: rgb(168, 142, 84);  
}

.bg-darkblue{
    background-color: rgb(39, 39, 107);
}
.bg-red{
  background-color: rgb(172, 71, 71);  
}
.bg-purple{
    background-color: rgb(104, 66, 125);
}


.text-green{
    color: rgb(40, 91, 40);;
}
.text-gold{
    color: rgb(168, 142, 84);  ;
}
.text-darkblue{
    color: rgb(39, 39, 107);;
}
.text-red{
   color: rgb(172, 71, 71);; 
}
.text-purple{
    color: rgb(104, 66, 125);
}
</style>