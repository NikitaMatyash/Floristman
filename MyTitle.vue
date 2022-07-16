<template>
	<h2>
		<slot></slot>
	</h2>
</template>

<script>
export default {

  name: 'my-title',

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
	h2 {
		font-weight: 700;
		font-size: 35px;
		line-height: 48px;
		text-align: center;
		color: #000000;
		margin-bottom: 30px;
	}
	@media (max-width: 808px) {
		h2 {
			font-size: 25px;
			line-height: 120%;
			margin-bottom: 30px;

		}
	}
</style>
