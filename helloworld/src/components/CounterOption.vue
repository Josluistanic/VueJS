<template>
    <h3>{{ counter }}</h3>
    <button @click="addCounter">Incrementar</button>
    <button @click="reduceCounter">Reducir</button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({

    name: 'CounterOption',

    data() {
        let counter = 0;
        return { counter };
    },

    methods: {
        /**
         * addCounter
         */
        addCounter() {
            this.counter++;
        },
        reduceCounter() {
            this.counter--;
        }
    },
})
</script>

<style></style>