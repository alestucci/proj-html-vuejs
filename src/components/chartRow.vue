<template>
  <div id="row">
		<div class="item-data">
			<h5>Black Jacket</h5>
			<h5>Stelle</h5>
			<h5>Prezzo</h5>
		</div>
		<div class="item-image">
			<img src="../assets/img/black_elegant_leather_jacket.jpg" alt="">
		</div>
  </div>
</template>

<script>
export default {
	name: "chartRow",
}
</script>

<style lang="scss" scoped>
#row {
	width: 100%;
	display: flex;
}
.item-data {
	width: 80%;
	display: flex;
	flex-direction: column;
	justify-content: flex-start;
}
.item-image {
	width: 20%;
	img {
		width: 100%;
	}
}
</style>