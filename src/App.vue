<template>
	<div id="app" role="main">
		<login v-if="showLogin"></login>
	</div>
</template>

<script>

function data() {
	return {
		showLogin: false,
	};
}

function mounted() {
	setTimeout(() => {
		this.showLogin = true;
	}, 800);
}

export default {
	name: 'app',
	components: {
		Login: () => import('./components/Login'),
	},
	data,
	mounted,
};
</script>

<style lang="scss">
html {
	font-family: Arial, Helvetica, sans-serif;
	font-size: 16px;
}

#app {
	align-items: center;
	display: flex;
	height: 100vh;
	justify-content: center;
}
</style>
