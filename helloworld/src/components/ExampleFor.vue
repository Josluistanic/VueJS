<template>
    <ul>
        <li v-for="country in countries" :key="country.code">{{ country.name }}</li>
    </ul>
</template>

<script lang="ts" setup>
import { Ref, ref } from 'vue';

interface ICountry {
    code: string,
    name: string,
    capital: string,
}

let countries: Ref<Array<ICountry>> = ref([
    { code: "es", name: "Spain", capital: "Madrid" },
    { code: "ec", name: "Ecuador", capital: "Quito" },
    { code: "co", name: "Colombia", capital: "Bogotá" }
]);
</script>

<style scoped></style>