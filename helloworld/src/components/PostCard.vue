<template>
    <div class="card">
        <h3>Título</h3>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nobis quidem dolor incidunt ab magnam. Ea praesentium
            maxime est at architecto deserunt nesciunt, nulla doloribus blanditiis amet, ipsa eveniet saepe odit!</p>
        <PostButton />
    </div>
</template>

<script lang="ts" setup>
import PostButton from './PostButton.vue'
</script>

<style scoped>
.card{
    border-radius: 15px;
    padding: 10px;
    margin: 5px;
    border: 1px solid #ccc;
}
</style>