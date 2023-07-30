<script>
export default {
    props: [
        "onTagsChange"
    ],

    data() {
        return {
            currentValue: '',
            tags: [],
        }
    },

    methods: {
        handleKeyDown(e) {
            if (e.key == 'Backspace' && this.currentValue === '') {
                this.tags.pop();
                this.onTagsChange(this.tags);
            }
        },
        handleSubmit() {
            if (this.currentValue !== '') {
                const exist = this.tags.some(item => item === this.currentValue);
                if (!exist) {
                    this.tags.push(this.currentValue);
                    this.currentValue = '';
                    this.onTagsChange(this.tags);
                }
            }
        },
        deleteTag(tag) {
            this.tags = this.tags.filter((item) => item !== tag);
            this.onTagsChange(this.tags);
        }
    }
}
</script>


<template>
    <div class="inputTag">
        <div class="tags">
            <div class="tag" v-for="(tag, index) in tags" :key="index">
                {{ tag }} <button @click="deleteTag(tag)"><strong>X</strong></button>
            </div>
        </div>
        <form @submit.prevent="handleSubmit">
            <input type="text" v-model="currentValue" @keydown="handleKeyDown" />
        </form>
    </div>
</template>


<style>
.inputTag {
    display: inline-flex;
    border: solid 1px #fff;
    padding: 10px;
    background-color: #fff;
    border-radius: 10px;
    height: 52px;
}

.tags {
    display: flex;
    gap: 3px;
    background-color: #fff;
}

.tags .tag {
    display: flex;
    padding: 3px 15px;
    gap: 10px;
    align-content: center;
    border-radius: 10px;
    background-color: #e3e3e3;
    color: #000;
}

.inputTag input {
    border: none;
    outline: none;
    padding: 0 5px;
}

.inputTag form {
    display: inline-flex;
}

.tag button {
    background-color: transparent;
    border: none;
    border-radius: 50px;
    cursor: pointer;
}

.tag button:hover {
    background-color: #ccc;
}
</style>