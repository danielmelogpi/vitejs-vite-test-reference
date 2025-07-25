<template>
<div>
    Child Counter: {{ counter.time }}
</div>
<div><button type="button" @click="$emit('counter-emit', counter)">Emit</button></div>


</template>
<script setup lang="ts">
import { onMounted, ref } from 'vue';

const counter = ref({time: 0});

onMounted(() => {
    setInterval(() => {
        counter.value.time++
    }, 1000)
})

</script>
