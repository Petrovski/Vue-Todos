<template>
	<header class="header">
		<h1>Todo List</h1>
		<img alt="Vue logo" src="../../assets/logo.png" />
	</header>
</template>

<script>
export default {
	name: "Header"
};
</script>

<style scoped>
.header {
	background: #333;
	color: #fff;
	text-align: center;
	padding: 10px;
}
.header a {
	color: #fff;
	padding-right: 5px;
	text-decoration: none;
}

img {
	height: 50px;
	width: 50px;
	margin-top: 20px;
}
</style>
