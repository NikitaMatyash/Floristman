<template>
	<div class="card">
		<p>{{card.title}}</p>
	</div>
</template>

<script>
export default {

  name: 'my-menu-section-item',
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
	.card {
		position: relative;
		display: flex;
		align-items: center;
		justify-content: flex-end;
		flex-direction: column;
		min-height: 278px;
		min-width: 278px;
		background-image: url('@/assets/rectangle.png');
		background-size: cover;
		background-repeat: no-repeat;
		cursor: pointer;
		transition: all 0.2s;
	}
	.card:hover {
		transform: translate(0px, -10px);
		transition: all 0.3s;
	}
	.card::before {
		content: '';
		position: absolute;
		bottom: 0;
		min-width: 100%;
		min-height: 62px;
		background: rgba(85, 183, 76, 0.8);
		border-radius: 13px 13px 0px 0px;
	}
	.card p {
		margin-bottom: 19px;
		font-weight: 500;
		font-size: 18px;
		line-height: 25px;
		color: #FFFFFF;
		z-index: 5;
	}
	@media (max-width: 1240px) {
    .card {
    	min-width: 233px;
    }
  }
  @media (max-width: 1064px) {
    .card {
    	min-width: 170px;
    	min-height: 230px;
    }
    .card p {
    	font-size: 15px
    }
  }
  @media (max-width: 808px) {
    .card {
    	min-width: 140px;
    	min-height: 200px;
    }
    .card p {
    	font-size: 12px
    }
  }
</style>
