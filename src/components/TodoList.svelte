<script lang="ts">
    import type { Todo } from "../models/todo";
    import TodoItem from "./TodoItem.svelte";

    export let todos: Todo[] = [];
</script>

<h3>Todo</h3>

<ul>
    {#each todos as todo, i}
        <TodoItem {todo} />
    {/each}
</ul>

<style>
    h3,
    ul {
        margin: 0.5em auto;
        width: fit-content;
    }

    ul {
        list-style-type: none;
    }
</style>
