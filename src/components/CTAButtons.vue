<template>
	<div>
		<button class="place-order-btn"><a href="#place-order">Place and order</a></button>
		<button class="check-menu-btn"><a href="#menu">Check our menu</a></button>
	</div>
</template>

<script>
export default {
  name: 'CTAButtons'
}
</script>

<style lang="scss" scoped>
div {
	max-width: 100%;
	display: flex;
	flex-flow: row wrap;
	justify-content: center;
	gap: 2rem;

	@media screen and (min-width: 920px) {
		justify-content: left;
	}
}

button {
  position: relative;
	z-index: 10;

	width: 80%;

  border: 0;
  outline: 0;
  border-radius: .5rem;

  font-size: 1.5rem;
  font-weight: bold;
	
	@media screen and (min-width: 768px) {
		width: auto;
	}

  a {
    display: block;
    padding: 1.2rem 2rem;
    width: 100%;
    color: white;
    text-decoration: none;
  }
}

.place-order-btn {
  background-color: #EBD948;

  a {
    color: black;
  }
}
.check-menu-btn {
  background-color: transparent;
}
//fix border around button to not change the size (border-box not working)
.check-menu-btn::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  z-index: -1;

  border-radius: .5rem;
  border: 4px solid white;
}
</style>