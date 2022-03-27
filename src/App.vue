<template>
    <div class="main">
        <p>This is Test {{ test }}</p>
        <input type="text" v-bind:value="test">
    </div>
    <button v-on:click="changeTest">Change</button>
</template>

<script>
export default {
    data() {
        return {
            test: 'Hello'
        }
    },
    methods: {
        changeTest() {
            this.test = 'World'
        }
    }
}
</script>

<style lang="scss" scoped>
.main {
    margin-bottom: 20px;

    p {
        color: red;
    }
    input {
        height: 40px;
        width: 200px;
    }
}
button {
    background-color: #ccc;
    border: 1px solid #999;
    border-radius: 3px;
    color: #333;
    cursor: pointer;
    font-size: 14px;
    font-weight: bold;
    padding: 5px 10px;
    text-transform: uppercase;
}
</style>