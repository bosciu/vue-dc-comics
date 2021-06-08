<template>
	<div class="comics-container">
		<div class="container">
			<div class="card" v-for="(card, index) in cards" :key="index"></div>
		</div>
	</div>
</template>

<script>
import cards from "../../JSON/dc-comics";
export default {
	name: "Comics",
	data: function () {
		return {
			cards
		};
	}
};
</script>

<style lang="scss" scoped>
@import "../style/mixins";
.comics-container {
	background-color: #1c1c1c;
	& > .container {
		@include flex-center("both");
		flex-wrap: wrap;
		.card {
			width: calc(100% / 6);
			height: 200px;
			margin: 3% 0;
			background-color: yellow;
			border: 3px solid red;
		}
	}
}
</style>
