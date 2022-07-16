<template>
	<div class="my-info-section__container">
		<my-title>4 веские причины выбрать нас!</my-title>
		<my-info-section-row :cards='cards'></my-info-section-row>
		<my-title>Как оформить заказ?</my-title>
		<my-info-section-row :cardsTwo='cardsTwo'></my-info-section-row>
	</div>
</template>

<script>
	import MyInfoSectionRow from '@/components/MyInfoSectionRow.vue'
export default {

	components: {
		MyInfoSectionRow,
	},

  name: 'my-info-section',

  data() {
    return {
    	cards: [
    		{id: 1, title: 'Качество', text: 'На Рыжском рынке предоставлены оптовые продавцы, которые торгуют самыми свежими цветами'},
    		{id: 2, title: 'Фото-отчет', text: 'Перед доставкой мы отправляем Вам фотографию готового букета'},
    		{id: 3, title: 'Цена', text: 'Да, у нас самые дешевые цены в онлайне! В 2-3 раза дешевле от обычных!'},
    		{id: 4, title: 'Время', text: 'Мы доставляем от 2-х часов! (Реальное время, а не маркетинговый ход) И принимаем заказы 24/7'},
    	],
    	cardsTwo: [
    		{id: 1, title: 'Оставьте заявку на сайте', text: 'Наш сотрудник свяжется с Вами для уточнения деталей вашего заказа'},
    		{id: 2, title: 'Фото-отчет', text: 'Перед доставкой мы пришлем фотографию готового Вашего букета, чтобы Вы убедились в его качестве. После утверждения вами заказа, курьер поедет по адресу'},
    		{id: 3, title: 'Способ оплаты', text: 'Наличными либо безналичным расчетом банковской картой после доставки'},
    		{id: 4, title: 'Доставка', text: 'Возьмём на себя все заботы по созданию, оформлению и доставке корпоративных букетов в обычные и праздничные дни за разумные деньги'},
    	],
    };
  },
};
</script>

<style lang="css" scoped>
	.my-info-section__container {
		margin-bottom: 75px;
	}
	@media (max-width: 1064px) {
		.my-info-section__container {
			margin-bottom: 45px;
		}
  }
  @media (max-width: 808px) {
		.my-info-section__container {
			margin-bottom: 35px;
		}
		
  }
</style>
