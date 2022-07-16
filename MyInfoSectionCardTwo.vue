<template>
	<div class="my-info-section-card__body">
		<img src="@/assets/icon/my-info-section-card--star.svg" alt="" class="my-info-section-card__icon">
		<h4 class="my-info-section-card__title">{{card.title}}</h4>
		<p class="my-info-section-card__text">{{card.text}}</p>
	</div>
</template>

<script>
export default {

  name: 'my-info-section-card-two',

  props: {
    card: {
      type: Object,
      required: true,
      default: null,
    },
  },

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
	.my-info-section-card__body {
		max-width: 278px;
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.my-info-section-card__icon {
		margin-bottom: 12px;
	}
	.my-info-section-card__title {
		margin-bottom: 3px;
		font-weight: 700;
		font-size: 18px;
		line-height: 25px;
		text-align: center;
		color: #000000;
	}
	.my-info-section-card__text {
		font-size: 18px;
		line-height: 25px;
		text-align: center;
		color: #000000;
	}
	@media (max-width: 1064px) {
		.my-info-section-card__icon {
			width: 50px;
		}
    .my-info-section-card__text {
			font-size: 13px;
			line-height: 130%;
		}
  }
</style>
