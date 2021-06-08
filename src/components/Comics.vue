<template>
	<div class="comics-container">
		<div class="container">
			<div id="label">Current series</div>
			<Card
				v-for="(card, index) in cardsList"
				:key="index"
				:img-src="card.thumb"
				:series="card.series"
			/>
			<Button text="Load More" />
		</div>
	</div>
</template>

<script>
import cardsList from "../../JSON/dc-comics";
import Card from "./Card";
import Button from "./../generic-components/Button";
export default {
	name: "Comics",
	components: {
		Card,
		Button
	},
	data: function () {
		return {
			cardsList
		};
	}
};
</script>

<style lang="scss" scoped>
@import "../style/mixins";
@import "../style/variables";
.comics-container {
	background-color: #1c1c1c;
	& > .container {
		@include flex-center("both");
		flex-wrap: wrap;
		position: relative;
		padding-bottom: 1%;
		#label {
			position: absolute;
			top: -4%;
			left: 0;
			padding: 12px 10px;
			background-color: $brandColor;
			text-transform: uppercase;
			font-weight: 700;
			font-size: 24px;
		}
	}
}
</style>
