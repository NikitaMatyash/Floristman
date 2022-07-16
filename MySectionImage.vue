<template>
	<div class="my-section-image__container">
		<img src="@/assets/my-section-image.png" alt="">
	</div>
</template>

<script>
export default {

  name: 'my-section-image',

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
	.my-section-image__container {
		margin-bottom: 75px;
	}
	img {
		max-width: 100%;
	}
	@media (max-width: 1064px) {
		.my-section-image__container {
			margin-bottom: 45px;
		}
  }
</style>
