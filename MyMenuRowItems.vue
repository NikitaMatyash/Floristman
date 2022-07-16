<template>
	<li v-for="item in items">
		<a href="#" class="menu__link">
			{{item.name}}
		</a>
	</li>
</template>

<script>
export default {

  name: 'my-menu-row-items',

  props: {
	  items: {
	    type: Array,
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
	.menu__link {
		font-size: 18px;
		line-height: 25px;
		color: #FFFFFF;
	}
	.menu__link:hover {
		color: #e3e3e3;
	}
	@media (max-width: 1240px) {
		.menu__link {
			font-size: 15px;
		}
	}
	@media (max-width: 1064px) {
    .menu__link {
			font-size: 12px;
		}
  }
  @media (max-width: 808px) {
  	.menu__link {
			font-size: 10px;
		}
  }
</style>
