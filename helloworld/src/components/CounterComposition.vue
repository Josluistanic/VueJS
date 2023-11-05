<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
    <button @click="reduceCounter">Reducir</button>
</template>


<script lang="ts" setup>
import { Ref, ref } from 'vue';

let counter: Ref = ref(0);

const addCounter = (): void => {
    counter.value++;
}

function reduceCounter(): void {
    counter.value--;
}

</script>