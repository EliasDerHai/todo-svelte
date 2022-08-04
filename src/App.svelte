<script lang="ts">
	import { Todo } from "./models/todo";
	import TodoList from "./components/TodoList.svelte";
	import "smelte/src/tailwind.css";

	const todos: Todo[] = [
		new Todo("hear about svelte"),
		new Todo("fiddle around with svelte"),
		new Todo("get bored"),
		new Todo("check out sth else..."),
	];
</script>

<link
	href="https://fonts.googleapis.com/css?family=Roboto:300,400,500|Material+Icons&display=swap"
	rel="stylesheet"
/>

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
