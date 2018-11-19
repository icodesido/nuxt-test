<template>
  <div class="container" :style="{ backgroundColor: `hsl(${x}, 80%, 50%)` }" @mousemove="xCoordinate">
    <h1>This is the product page</h1>
    <p><nuxt-link to="/">Home page</nuxt-link></p>
		<p>Pixels across: {{ x }}</p>
  </div>
</template>

<script>
export default {
  data: () => ({
    x: 0
  }),

	methods: {
		xCoordinate(e) {
			this.x = e.clientX;
		}
	}	
}
</script>

<style scoped>
  .container {
    background: #222;
  }
</style>