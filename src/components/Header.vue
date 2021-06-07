<template>
	<header class="container">
		<div id="logo-container">
			<img src="../assets/img/dc-logo.png" alt="" />
		</div>
		<nav>
			<ul>
				<li><a href="#">Characters</a></li>
				<li class="active"><a href="#">Comics</a></li>
				<li><a href="#">Movies</a></li>
				<li><a href="#">Tv</a></li>
				<li><a href="#">Games</a></li>
				<li><a href="#">Collectibles</a></li>
				<li><a href="#">Videos</a></li>
				<li><a href="#">Fans</a></li>
				<li><a href="#">News</a></li>
				<li><a href="#">Shop</a></li>
			</ul>
		</nav>
	</header>
</template>

<script>
export default {
	name: "Header"
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
.container {
	display: flex;
	justify-content: space-between;
	align-items: center;
	overflow: hidden;
	img {
		padding: 10% 0;
	}
	nav {
		flex-grow: 1;
		ul {
			display: flex;
			justify-content: flex-end;
			li {
				margin-left: 3%;
				font-size: 14px;
				font-weight: 600;
				text-transform: uppercase;
				cursor: pointer;
				color: #464646;
				&.active {
					position: relative;
					color: $brandColor;
				}
				&.active::after {
					content: "";
					position: absolute;
					top: 65px;
					width: 100%;
					height: 20px;
					display: block;
					background: $brandColor;
				}
			}
		}
	}
}
</style>
