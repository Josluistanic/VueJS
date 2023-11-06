<template>
    <p :style="{
        backgroundColor: '#ccc',
        color: c,
    }">El mensaje se ha envíado con éxito</p>
    <button @click="changeColor">Cambiar color</button>
</template>

<script lang="ts">
import { Ref, defineComponent, ref } from 'vue';
export default defineComponent({
    name: 'ClassBind',
    setup() {
        let c: Ref<string> = ref('#fff');

        function changeColor() {
            c.value = '#ff0000';
        }

        return { c, changeColor };
    }
});
</script>

<style scoped></style>