<template>
  <div>
    <form @submit="addTodo">
			<input type="text" v-model="title" name="title" placeholder="Add Todo..." />
			<input type="submit" value="Submit" class="btn" />
		</form>
	</div>
</template>

<script>
// import uuid from "uuid";

export default {
	name: "AddTodo",
	methods: {
		addTodo(event) {
			event.preventDefault();
			const newTodo = {
				// id: uuid.v4(), // JSON placeholder generates us an ID like a database would
				title: this.title,
				completed: false
			};
			// Send up to parent by emitting an event
			this.$emit("add-todo", newTodo);

			this.title = "";
		}
	},
	data() {
		return {
			title: ""
		};
	}
};
</script>

<style scoped>
form {
	display: flex;
}
input[type="text"] {
	flex: 10;
	padding: 5px;
}
input[type="submit"] {
	flex: 2;
}
</style>
