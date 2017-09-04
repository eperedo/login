<template>
	<div id="app" role="main">
		<login></login>
	</div>
</template>

<script>

export default {
	name: 'app',
	components: {
		Login: () => import('./components/Login'),
	},
};
</script>

<style lang="scss">
html {
	font-family: Arial, Helvetica, sans-serif;
	font-size: 16px;
}
</style>
