<script lang="ts">
    import { Todo } from "../models/todo";
    import TodoItem from "./TodoItem.svelte";

    export let todos: Todo[] = [];
    let newTodoDescription = "";

    const add = () => {
        todos = [...todos, new Todo(newTodoDescription)];
        newTodoDescription = "";
    };
</script>

<h3>Todo</h3>

<ul>
    {#each todos as todo, i}
        <TodoItem {todo} />
    {/each}
</ul>

<form on:submit|preventDefault={add}>
    <input
        type="text"
        bind:value={newTodoDescription}
        required
        placeholder="enter new todo"
    />
    <button type="submit">Add</button>
</form>

<style>
    h3,
    ul,
    form {
        margin: 0.5em auto;
        width: fit-content;
    }

    ul {
        list-style-type: none;
    }

    form {
        border: 1px MediumSeaGreen solid;
        border-radius: 5px;
        padding: 10px;
    }
</style>
