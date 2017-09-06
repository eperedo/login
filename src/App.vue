<template>
	<div id="app" role="main">
		<login></login>
	</div>
</template>

<script>

import Login from './components/Login';

export default {
	name: 'app',
	components: {
		Login,
	},
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
