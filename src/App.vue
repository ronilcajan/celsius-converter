
<script setup>
    import DegreesInputBox from './components/DegreesInputBox.vue'
    import TemparatureSelector from './components/TemperatureSelector.vue'
    import ConvertButton from './components/ConvertButton.vue'
    import Result from './components/Result.vue'

    import { ref } from 'vue';


    const inputDegree = ref('');
    const temperature = ref(1);

    const resultData = ref('');

    const convertData = () => {
        if(inputDegree.value > 0){
            if(temperature.value == '2') {
                resultData.value = Number(inputDegree.value) + 273.15 +" °K";
            }
            if(temperature.value == '1') {
                resultData.value = (Number(inputDegree.value) * 1.8) + 32 + " °F";
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
            <DegreesInputBox v-model:degree="inputDegree"/>
            <TemparatureSelector v-model:temp="temperature" />
            <ConvertButton @convert-degrees="convertData" />
            <Result :result-degree="resultData" />
        </div>
    </div>

</template>
