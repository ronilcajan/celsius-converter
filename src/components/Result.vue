<script setup>    
    const props = defineProps({
        resultDegree: {
            type: String,
            required: true
        }
    })
</script>

<template>

<p>Result: <span >{{ resultDegree }}</span></p>

</template>