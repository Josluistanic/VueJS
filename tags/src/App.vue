<script>
 import InputTag from './components/inputTag.vue';

export default {
    components: {
        InputTag
    },
    methods: {
        handleOnTagsChange(tags) {
            console.log(tags);
        }
    }
}
</script>

<template>
    <InputTag :onTagsChange="handleOnTagsChange" />
</template>

<style scoped></style>
