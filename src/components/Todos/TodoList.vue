<template>
    <div>

        <h1>todoList</h1>
        <div
                v-for="(todo, i) in todoArr"
                :key="`${todo}${i}`"
        >


            <TodoItem
                    :todo="todo"
                    @deleteTodo="deleteTodo"

            />

        </div>
        <Input
        @add="add"
        />

    </div>
</template>

<script>
    import TodoItem from "@/components/Todos/TodoItem";
    import Input from "@/components/Input";

    export default {
        name: 'TodoList',
        components: {
            TodoItem,
            Input
        },

        data() {
            return {
                todoArr: [],
            }
        },


        methods: {
            deleteTodo(event) {
                for (var i = 0; i < this.todoArr.length; i++) {
                    if (this.todoArr[i] === event) {
                        this.todoArr.splice(i, 1);
                        console.log(event)
                    }
                }
            },

            add(event) {
                this.todoArr.push(event);
            }


        },


    }
</script>
