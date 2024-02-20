
<script setup>
    import { ref } from 'vue';


    const degree = ref('');
    const temperature = ref(1);

    const result = ref('');


    const convertDegrees = () => {
        console.log(degree);
        if(degree.value > 0){
            if(temperature.value == '1') {
                result.value = Number(degree.value) + 273.15 + " °F";
            }
            if(temperature.value == '2') {
                result.value = (Number(degree.value) * 1.8) + 32 + " K";
            }
        }else{
            alert('Please enter greater than 0!');

        }
    }

</script>

<template>

    <div class="flex justify-center items-center h-screen">
        <div class="flex items-center gap-2">
            <p>Celsius :</p>
            <input type="number" v-model="degree" placeholder="Enter celsius"  class="rounded border p-2 border-black">
            <select class="border border-black rounded p-2" v-model="temperature">
                <option value="1">Fahrenheit</option>
                <option value="2">Kelvin</option>
            </select>
            <button type="button" class="bg-sky-600	py-2 px-3 text-white rounded" @click="convertDegrees">Convert</button>
            <p>Result: <span >{{ result }}</span></p>

        </div>
    </div>

</template>
