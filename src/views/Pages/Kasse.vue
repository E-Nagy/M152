<script setup>
import { computed, ref } from "vue";

//main array
const log = ref([
    {
        id: 1,
        text: 'Startsaldo',
        value: 1500
    },
    {
        id: 2,
        text: 'Bus-Abo',
        value: -79
    },


])

//round
function roundTo05(number) {
    return (Math.ceil(number * 20) / 20).toFixed(2);
}

//Add to array
function newEntry() {
    const newElement = {
        text: newText.value,
        value: parseFloat(newValue.value),
        id: ++currentId.value

    }

    log.value.push(newElement)

    //reset form
    newText.value = ''
    newValue.value = ''
    newTextField.value.focus()
}

//delete from Array
function deleteEntry(id) {
    log.value = log.value.filter((element) => {
        return element.id !== id
    })
}

//calculate Sums
const totalIncome = computed(()=>{
    let sum = 0
    log.value.forEach(el =>{
        if (el.value > 0){
            sum += el.value
        }
    })
    return sum;
})

const totalExpenses = computed(()=>{
    let sum = 0
    log.value.forEach(el =>{
        if (el.value < 0){
            sum += el.value
        }
    })
    return sum;
})

const totalSum = computed(() =>{
    return totalIncome.value + totalExpenses.value;
})

//Reactive Variables
const newTextField = ref();
const newText = ref();
const newValue = ref();
const currentId = ref(2)

</script>

<template>
    <h1>Meine Kasse</h1>

    <table>

        <tr>
            <th>Bezeichnung</th>
            <th>Eingang</th>
            <th>Ausgang</th>
            <th></th>
        </tr>

        <tr v-for="singlog in log" :key="singlog.id">
            <td>{{ singlog.text }}</td>
            <td class="sum"><span v-if="singlog.value > 0" class="positive">{{ roundTo05(singlog.value) }}</span></td>
            <td class="sum"><span v-if="singlog.value < 0" class="negative">{{ roundTo05(singlog.value) }}</span></td>
            <td class="button-container"><button class="delete-button" @click="deleteEntry(singlog.id)">x</button></td>
        </tr>

        <tr>
            <th>Summen</th>
            <th>{{roundTo05( totalIncome) }}</th>
            <th>{{ roundTo05(totalExpenses) }}</th>
            <th>Total:</th>
        </tr>
        <tr>
            <td></td>
            <td></td>
            <td></td>
            <td>{{ roundTo05(totalSum) }}</td>
        </tr>

    </table>

    <div class="form">
        <h2>Neuer Eintrag</h2>

        <label for="text">Bezeichnung</label>
        <input ref="newTextField" v-model="newText" type="text" name="text" id="text" @keyup.enter="newEntry">
        <label for="text">Betrag</label>
        <input v-model="newValue" type="number" name="text" id="text" @keyup.enter="newEntry">
        <button @click="newEntry">Hinzufügen</button>
    </div>
</template>

<style lang="scss">
h1 {
    margin: auto;
    margin-bottom: 20px;
}

.form {
    color: #f2f2f2;
    display: flex;
    flex-direction: column;
    width: fit-content;
    height: fit-content;
    margin-top: 50px;
    margin-left: auto;
    margin-right: auto;
    padding: 15px;
    border-radius: 10px;
    background-color: #8a8a8a;

    label {
        margin-bottom: 5px;
    }

    input {
        margin-top: 0;
        width: 100%;
        margin-bottom: 15px;
    }


}

table {
    margin: auto;
    font-family: Arial, Helvetica, sans-serif;
    border-collapse: collapse;
    width: auto;


    td,
    th {
        border: 1px solid #ddd;
        padding: 8px;
        height: fit-content;

        .delete-button {
            margin-left: 0;
            margin-top: 0;
            margin-bottom: 0;
            width: 40px;
            padding: 0;
        }

        .delete-button:hover {
            cursor: pointer;
        }


    }

    tr:nth-child(even) {
        background-color: #f2f2f2;
    }

    th {
        padding-top: 12px;
        padding-bottom: 12px;
        text-align: left;
        background-color: #8a8a8a;
        color: white;

    }

    .sum {
        text-align: right;
    }


    .positive {
        color: rgb(77, 126, 47);
    }

    .negative {
        color: rgb(195, 75, 75);
    }

}
</style>