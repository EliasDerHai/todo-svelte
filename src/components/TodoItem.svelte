<script lang="ts">
    import type { Todo } from "../models/todo";

    export let todo: Todo;
</script>

<li>
    <input
        type="checkbox"
        bind:checked={todo.done}
        on:change={() => console.log(todo)}
    />
    <span class:done={todo.done}>{todo.description}</span>
</li>

<style>
    .done {
        text-decoration-line: line-through;
    }
</style>
