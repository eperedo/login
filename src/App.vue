<template>
	<div id="app">
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
	font-size: 16px;
}
</style>
