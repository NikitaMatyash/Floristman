<template>
	<a class="slider-item" >
		<img class='slider-item__img' src="@/assets/slider-img.png">
		<h4 class="slider-item__title">{{item.title}}</h4>
		<div v-if="item.price > 0">
			<span class="price">{{item.price}}грн</span>
			<span class="discount">{{item.discount}}грн</span>
		</div>
		<div v-else='item.price === 0'><p>Цены пока нет</p></div>
		<button :class="{ 'not-active': item.price === 0 }" class="slider-item__btn">
			<p v-if="item.price === 0">Товара нет</p>
			<p v-else>Добавить в корзину</p>
		</button>
	</a>
</template>

<script>
export default {

  name: 'my-slider-item',

  props: {
    item: {
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

	.slider-item {
		position: relative;
		display: flex;
		justify-content: flex-end;
		flex-direction: column;
		max-height: 485px;
		max-width: 278px;
		cursor: pointer;
		transition: all 0.2s;
	}
	.slider-item__img {
		margin-bottom: 24px;
	}
	.slider-item__title {
		margin-bottom: 24px;
		font-weight: 700;
		font-size: 22px;
		line-height: 30px;
		color: #000000;
	}
	.slider-item div {
		margin-bottom: 24px;
	}
	.price {
		font-size: 25px;
		line-height: 30px;
		color: #000000;
		margin-right: 10px;
	}
	.discount {
		font-size: 19px;
		line-height: 30px;
		text-decoration-line: line-through;
		color: #898989;
	}
	.slider-item__btn {
		font-weight: 700;
		font-size: 18px;
		line-height: 25px;
		color: #FFFFFF;
		padding: 12px 43px;
		background: #55B74C;
		border-radius: 7px;
		width: 100%;
		max-height: 50px;
	}
	.slider-item div p {
		font-size: 22px;
		line-height: 30px;
		color: #000000;
		margin-right: 10px;
	}
	.not-active {
		background: #879586;
	}
	@media (max-width: 1240px) {
    .slider-item__btn {
    	padding: 10px;
    }
  }
  @media (max-width: 1064px) {
  	.slider-item__img {
			margin-bottom: 20px;
		}
  	.slider-item__title {
  		margin-bottom: 19px;
  	}
  	.slider-item div {
			margin-bottom: 14px;
		}
  	.price {
  		font-size: 20px;
  	}
  	.discount {
  		font-size: 14px;
  	}
  	.slider-item div p {
			font-size: 18px;
		}
    .slider-item__btn {
    	font-size: 14px;
    	padding: 10px 5px;
    }
  }
  @media (max-width: 808px) {
  	.slider-item__img {
			margin-bottom: 10px;
		}
  	.slider-item__title {
  		font-size: 15px;
  		line-height: 120%;
  		margin-bottom: 10px;
  	}
  	.slider-item div {
			margin-bottom: 10px;
		}
  	.price {
  		font-size: 14px;
  		line-height: 120%;
  	}
  	.discount {
  		font-size: 12px;
  		line-height: 120%;
  	}
  	.slider-item div p {
			font-size: 14px;
  		line-height: 120%;
		}
		.slider-item__btn {
    	font-size: 10px;
  		line-height: 120%;
    	padding: 10px 8px;
    }
  }
</style>
