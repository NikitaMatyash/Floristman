<template>
	<footer class="footer">
		<div class="footer__container">
			<div class="footer__info-row">
				<my-footer-info-block v-for="block in blocks" :block="block" :key="block.id"></my-footer-info-block>
			</div>
		</div>
	</footer>
</template>

<script>
	import MyFooterInfoBlock from "@/components/MyFooterInfoBlock.vue";

export default {

	components: {
		MyFooterInfoBlock,
	},

  name: 'my-footer',

  data() {
    return {
    	blocks: [
    		{id: 1, title: 'Информация', linksName: [
    			{name: 'О нас'},
    			{name: 'Доставка'},
    			{name: 'Политика безопасности'},
    			{name: 'Условия соглашения'},
    		]},
    		{id: 2, title: 'Каталог', linksName: [
    			{name: 'Цветы'},
    			{name: 'Подарки'},
    			{name: 'Фруктовые корзины'},
    			{name: 'Воздушные шарики'},
    			{name: 'Комнатные растения'},
    			{name: 'Сладости'},
    			{name: 'Услуги'},
    			{name: 'Аксессуары'},
    		]},
    		{id: 3, title: 'Личный кабинет', linksName: [
    			{name: 'Личный кабинет'},
    			{name: 'Корзина'},
    		]},
    		{id: 4, title: 'Адрес', linksName: [
    			{name: 'г. Киев'},
    		]},
    		{id: 4, title: 'Телефоны', linksName: [
    			{name: '+7 968 765-70-07'},
    			{name: '+7 925 965-70-07'},
    		]},
    	],
    };
  },
};
</script>

<style lang="css" scoped>
	.footer {
		background-color: #2B2B2B;
		padding: 57px 20px 87px;
	}
	.footer__info-row {
		display: flex;
		gap: 100px;
	}
	@media (max-width: 1240px) {
    .footer__info-row {
    	justify-content: space-between;
    	gap: 50px;
    }
  }
  @media (max-width: 1064px) {
    .footer__info-row {
    	gap: 30px;
    }
    .footer {
			padding: 40px 10px;
		}
  }
  @media (max-width: 808px) {
  	.footer {
			background-color: #2B2B2B;
			padding: 30px 20px;
		}
  	.footer__info-row {
    	gap: 15px;
    }
  }
</style>
