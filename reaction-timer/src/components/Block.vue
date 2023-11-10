<template>
	<div class="block">
		Click me!
	</div>
</template>

<script>
export default {
	props: ['delay'],
}
</script>

<style>
.block {
	width: 400px;
	border-radius: 20px;
	background: rgb(253, 0, 0);
	color: white;
	text-align: center;
	padding: 100px 0;
	margin: 50px auto;
}

</style>