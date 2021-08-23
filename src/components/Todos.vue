<template>
	<div>
		<div v-for="todo in todosList"  v-bind:key="todo.id">
			<TodoItem v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)" />
		</div>
	</div>
</template>

<script>
import TodoItem from './TodoItem.vue'

	export default {
		name: 'Todos',
		props: ['todosList'], 
		components: {TodoItem}
	}
	
</script>

<style>
</style>