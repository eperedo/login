<template>
	<section class="login-container">
		<section class="login-content">
			<login-image></login-image>
			<login-form></login-form>
		</section>
	</section>
</template>

<script>

// import LoginForm from './LoginForm';
// import LoginImage from './LoginImage';

export default {
	name: 'Login',
	components: {
		LoginForm: () => import('./LoginForm'),
		LoginImage: () => import('./LoginImage'),
	},
};
</script>

<style lang="scss" scoped>
.login-container {
	background-image: radial-gradient(50% 84%, map-get($colors, green) 13%, map-get($colors, dark-green) 87%);
	max-height: 800px;
	margin: auto;
	padding: 59px 85px;
	width: 800px;
}

.login-content {
	display: flex;
}
</style>


