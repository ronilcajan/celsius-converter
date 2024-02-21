<script setup>
    const model = defineModel('temp')
</script>
<template>
    <select class="border border-black rounded p-2"  v-model="model">
                <option value="1">Fahrenheit</option>
                <option value="2">Kelvin</option>
            </select>
</template>