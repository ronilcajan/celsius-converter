<script setup>
    const degree = defineModel('degree')
</script>

<template>
    <input type="number" v-model="degree" placeholder="Enter celsius"  class="rounded border p-2 border-black">
</template>