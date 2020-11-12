<template>
    <div class="todo">
        <h1>todo item componnent</h1>
        <h3>{{todo}}</h3>
        <button @click="removeTodo(todo)">remove</button>
    </div>
</template>

<script>
    export default {
        name: 'TodoItem',
        props: {
            todo: {
                type: String
            },
        },

        methods: {
            removeTodo(todo) {
                this.$emit('deleteTodo', todo);
            }
        }
    }

</script>

<style>
    .todo {
        border: solid #5B6DCD 10px;
        background: hotpink;
    }

</style>
