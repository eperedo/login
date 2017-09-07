<template>
	<div id="app" role="main">
		<login v-if="showLogin"></login>
	</div>
</template>

<script>

// import Login from './components/Login';

function created() {
	setTimeout(() => {
		this.showLogin = true;
	}, 100);
}

function data() {
	return {
		showLogin: false,
	};
}

export default {
	name: 'app',
	components: {
		Login: () => import('./components/Login'),
	},
	data,
	created,
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
