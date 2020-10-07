<template>
	<section id="menu" class="container">
		<ul v-for="category in menu" :key="category.name">
			<h1>{{ category.name }}</h1>
			<li v-for="(menu_item, index) in category.items" :key="category.name+index">
				<h2>{{ menu_item.name }}</h2>
				<span>{{ menu_item.price }}</span>
				<p v-if="menu_item.description">{{ menu_item.description }}</p>
			</li>
		</ul>
	</section>
</template>

<script>
export default {
	name: "Menu",
	props: {
		menu: Array
	}
}
</script>

<style lang="scss" scoped>
section {
	max-width: 1100px;

	display: block;

  columns: 400px 2;
  column-gap: 5%;
  column-fill: balance;
}

ul {
	margin: 0;
	padding: 0;
	min-width: 100%;

	position: relative;
	display: inline-block;
	page-break-inside: avoid;
	break-inside: avoid-column;

	list-style: none;

	h1 {
		padding: .5rem;
		color: black;
		background-color: #fff;
	}

	li {
		padding: 0 1.5rem;
		margin-bottom: 1.5rem;
		display: grid;
		grid-template:
								"name price" auto
								"desc price" auto / auto min-content;

		text-align: left;
		align-items: center;

		h2 {
			margin: 0;
			font-size: 1.5rem;
			grid-area: name;
		}

		span {
			padding: 0 .5rem;
			font-size: 1.5rem;
			font-weight: bold;
			grid-area: price;

			&::before {
				content: '$';
			}
		}

		p {
			margin: 0;
			grid-area: desc;
		}
	}
}
</style>