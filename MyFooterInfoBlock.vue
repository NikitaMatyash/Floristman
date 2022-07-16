<template>
	<ul class="my-footer-info-block__list">
		<h4 class="my-footer-info-block__title">{{block.title}}</h4>
		<li v-for="link in block.linksName" class="my-footer-info-block__item">
			<p v-if="link.name === 'г. Киев'" class="my-footer-info-block__link">{{link.name}}</p>

			<a v-else-if="link.name === '+7 968 765-70-07'" href="tel:+79687657007" class="my-footer-info-block__link">
				<img src="@/assets/icon/telephone-footer.svg">{{link.name}}
			</a>

			<a v-else-if="link.name === '+7 925 965-70-07'" href="tel:+79259657007" class="my-footer-info-block__link">
				<img src="@/assets/icon/telephone-footer.svg">{{link.name}}
			</a>

			<a v-else href="#" class="my-footer-info-block__link">
				{{link.name}}
			</a>
		</li>
	</ul>
</template>

<script>
export default {

  name: 'my-footer-info-block',

  props: {
    block: {
      type: Object, Array,
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
	.my-footer-info-block__list {
		display: flex;
		flex-direction: column;
	}
	.my-footer-info-block__list li:last-child {
		margin-bottom: 0;
	}
	.my-footer-info-block__title {
		font-weight: 700;
		font-size: 18px;
		line-height: 25px;
		color: #55B74C;
		margin-bottom: 20px;
	}
	.my-footer-info-block__item {
		margin-bottom: 15px;
	}
	.my-footer-info-block__link {
		font-size: 18px;
		line-height: 25px;
		color: #898989;
	}
	.my-footer-info-block__link img {
		margin-right: 15px;
	}
	@media (max-width: 1240px) {
    .my-footer-info-block__title {
    	font-size: 16px;
    	margin-bottom: 10px;
    }
    .my-footer-info-block__item {
			margin-bottom: 5px;
		}
    .my-footer-info-block__link {
			font-size: 13px;
		}
		.my-footer-info-block__link img {
			width: 17px;
		}
  }
  @media (max-width: 808px) {
  	.my-footer-info-block__title {
    	font-size: 13px;
    	margin-bottom: 10px;
    }
    .my-footer-info-block__link {
			font-size: 10px;
		}
		.my-footer-info-block__link img {
			width: 13px;
			margin-right: 10px;
			margin-top: 5px;
		}

  }
</style>
