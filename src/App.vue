<template>
    <div id="app">
        <TodoList />
<!--        <Input/>-->
    </div>
</template>

<script>
    import TodoList from "@/components/Todos/TodoList";
    // /import Input from "@/components/Input";

    export default {
        name: 'App',
        components: {
            TodoList,
            // Input
        },

    }
</script>

<style>

</style>
