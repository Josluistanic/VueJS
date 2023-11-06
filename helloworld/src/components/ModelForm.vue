<template>
    <form action="#" method="post">
        <label for="nombre">Nombre</label>
        <input type="text" name="nombre" id="nombre" autofocus v-model="inputText">
    </form>
    <h3>
        {{ inputText }}
    </h3>
</template>

<!-- Composition API -->
<!-- <script lang="ts" setup>
import { Ref, ref } from 'vue';

let inputText: Ref<string> = ref('');
</script>  -->

<!-- Composition API -->
<!-- <script lang="ts">
import { Ref, defineComponent, ref } from 'vue';
export default defineComponent({
    name: 'ModelForm',
    setup() {
        let inputText: Ref<string> = ref('');
        return { inputText };
    }
});
</script>  -->
 
<!-- Option API -->
<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
    name: 'ModelForm',
    data() {
        return {
            inputText: '',
        }
    }
});
</script>


<style scoped>
label {
    display: block;
}
</style>