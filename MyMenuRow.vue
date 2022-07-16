<template>
	<div class="menu__container">
		<div class="menu">
			<ul class="menu__list">
				<my-menu-row-items :items='items'></my-menu-row-items>
			</ul>
		</div>
	</div>
</template>

<script>
	import MyMenuRowItems from '@/components/MyMenuRowItems.vue'
export default {

	components: {
		MyMenuRowItems,
	},

  name: 'my-menu-row',

  data() {
    return {
    	items: [
    		{id: 1, name: 'Цветы'},
    		{id: 2, name: 'Подарки'},
    		{id: 3, name: 'Фруктовые корзины'},
    		{id: 4, name: 'Воздушные шарики'},
    		{id: 5, name: 'Комнатные растения'},
    		{id: 6, name: 'Сладости'},
    		{id: 7, name: 'Услуги'},
    		{id: 8, name: 'Аксессуары'},
    	],
    };
  },
};
</script>

<style lang="css" scoped>
	.menu__container {
		margin-bottom: 20px;
	}
	.menu {
		background: linear-gradient(180deg, #55B74C 0%, #4BA043 162.75%);
		border-radius: 7px;
		padding: 13px 33px;
	}
	.menu__list {
		display: flex;
		justify-content: space-between;
		gap: 35px;
	}
	@media (max-width: 1064px) {
		.menu__list {
			gap: 10px;
		}
  }
  @media (max-width: 808px) {
  	.menu {
  		padding: 10px 15px;
  	}
  	.menu__list {
			gap: 5px;
		}
  }
</style>
