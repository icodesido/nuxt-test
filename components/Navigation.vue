<template>
	<nav>
	  <div class="title">
	    <nuxt-link exact to="/">Home page</nuxt-link>
	    <nuxt-link to="/product">Product page</nuxt-link>
	    <nuxt-link to="/contact">Contact page</nuxt-link>
	  </div>
	</nav>
</template>

<style>
	.title {
		padding: 20px;
		display: flex;
		justify-content: space-evenly;
	}
</style>