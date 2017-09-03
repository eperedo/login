<template>
	<div class="login-form">
		<form>
			<legend>The form here</legend>
		</form>
	</div>
</template>

<script>
export default {
	name: 'login-form',
};
</script>

<style lang="scss" scoped>
.login-form {
	background-color: map-get($colors, yellow);
	width: 100%;
}
</style>

