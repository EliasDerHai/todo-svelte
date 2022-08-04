<script lang="ts">
	import { Todo } from "./models/todo";
	import TodoList from "./components/TodoList.svelte";

	const todos: Todo[] = [
		new Todo("hear about svelte"),
		new Todo("fiddle around with svelte"),
		new Todo("get bored"),
		new Todo("check out sth else..."),
	];
	
</script>

<main>
	<TodoList {todos} />
</main>

<style>
	main {
		height: 100%;
		display: flex;
		justify-content: center;
		flex-direction: column;
	}
</style>
