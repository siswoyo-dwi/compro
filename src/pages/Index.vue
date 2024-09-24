<template>
    Index
</template>

<script>
export default {
	computed: {
		color() {
			if (this.$appState.colorScheme === 'light') return 'dark';
			return 'light';
		}
	}
}
</script>

<style scoped>

</style>