<template>
    <div id="app">
        <input type="text" v-model="value">
        <button @click="addTodo(value)">add</button>
    </div>
</template>

<script>


    export default {
        name: 'Input',
        components: {
        },
        data() {
            return {
                value:''
            };
        },

        methods:{
            addTodo(value){
                this.$emit('add', value);
            }
        }

    }
</script>

<style>

</style>
