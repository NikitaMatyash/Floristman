<!-- :style="{'margin-bottom': 75 + 'px'}" -->
<template>
	<section>
		<div class="slider__container">
			<swiper
				:slides-per-view="4"
	    	:space-between="30"
	    	:breakpoints="swiperOptions.breakpoints"
				:navigation="true" 
				:modules="modules" 
				class="mySwiper"
			>
		    <swiper-slide v-for='item in items'>
		    	<my-slider-item :item='item'></my-slider-item>
		    </swiper-slide>	    
		  </swiper>
		</div>
	</section>
</template>

<script>
	import MySliderItem from '@/components/MySliderItem.vue'

	import { Swiper, SwiperSlide } from "swiper/vue";
	import "swiper/css";
	import "swiper/css/navigation";
	import { Navigation } from "swiper";

export default {

	components: {
		MySliderItem,
		Swiper,
    SwiperSlide,
	},
	setup() {
    return {
      modules: [Navigation],
      swiperOptions: {
      	breakpoints: {
      		808: {
      			spaceBetween: 10,
      		}
      	}
      }
    };
  },

  name: 'my-slider',

  data() {
    return {
    	items: [
    		{id: 1, title: 'Корзина роз', price: 0, discount: 0},
    		{id: 2, title: 'Корзина роз', price: 150, discount: 190},
    		{id: 3, title: 'Корзина роз', price: 150, discount: 190},
    		{id: 4, title: 'Корзина роз', price: 0, discount: 190},
    		{id: 5, title: 'Корзина роз', price: 150, discount: 190},
    		{id: 6, title: 'Корзина роз', price: 150, discount: 190},
    		{id: 7, title: 'Корзина роз', price: 0, discount: 190},
    		{id: 8, title: 'Корзина роз', price: 150, discount: 190},
    	]
    };
  },
};
</script>

<style lang="css">
	section {
		margin-bottom: 75px;
	}
	.mySwiper {
		width: 100%;
		height: 100%;
	}
	.swiper-button-prev,
	.swiper-button-next {
		color: #fff;
	}
	@media (max-width: 1064px) {
    section {
    	margin-bottom: 45px;
    }
  }
  @media (max-width: 808px) {
    section {
    	margin-bottom: 35px;
    }
  }
</style>
