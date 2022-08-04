<script lang="ts">
    import type { Todo } from "../models/todo";
    import Toasts from "./toast/Toasts.svelte";
    import { addToast } from "./toast/store";

    export let todo: Todo;

    const toast = () => {
        const message = todo.done
            ? `You finished ${todo.description} - Great job!`
            : "Not yet done?";
        addToast({ message, timeout: 750 });
    };
</script>

<Toasts />

<li>
    <input type="checkbox" bind:checked={todo.done} on:change={toast} />
    <span class:done={todo.done}>{todo.description}</span>
</li>

<style>
    .done {
        text-decoration-line: line-through;
    }
</style>
