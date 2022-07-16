<template>
	<header>
		<div class="header__container">
			<nav class="nav">
				<ul class="nav__list">
					<li><a href="#" class="nav__link">Контакты</a></li>
					<li><a href="#" class="nav__link">О нас</a></li>
					<li><a href="#" class="nav__link">Доставка</a></li>
					<li><a href="#" class="nav__link">Политика безопасности</a></li>
					<li><a href="#" class="nav__link">Условия соглашения</a></li>
				</ul>
				<a href="#" class="user-account">
					<p>Личный кабинет</p>
					<img src="@/assets/icon/user_icon.svg" alt="">
				</a>
			</nav>
			<div class="header__row">
				<a href="#" class="logo"><img src="@/assets/logo.png" alt=""></a>
				<div class="address">
					<p>Адрес магазина</p>
					<span>г. Киев</span>
				</div>
				<div class="tel">
					<p>Главный офис</p>
					<a href="tel:+79687657007"><img src="@/assets/icon/telephone.svg" alt="">+7 968 765-70-07</a>
				</div>
				<div class="tools">
					<my-input 
						class="header__iput" 
						:class="{ visibility: visibilityValue}" 
						ref="input" 
						placeholder="Найти..."
					>
					</my-input>
					<a class="search" href="#" @click="addVisibility"><img src="@/assets/icon/search.svg" alt=""></a>
					<a class="shopping-bag" href="#"><img src="@/assets/icon/shopping-bag.png" alt=""></a>
					<a class="favorits" href="#"><img src="@/assets/icon/favorits.svg" alt=""></a>
				</div>
			</div>
		</div>
	</header>
	
</template>

<script>
export default {

  name: 'my-header',

  data() {
    return {
    	visibilityValue: false,
    };
  },
  methods: {
    blurInput() {
    	if (this.visibilityValue === false) {
      	this.$refs.input.$el.blur();
    	}
    },
    focusInput() {
    	this.$refs.input.$el.focus();
    },
    addVisibility() {
      this.visibilityValue = !this.visibilityValue;
      setTimeout(this.blurInput, 100);
      setTimeout(this.focusInput, 100);
    },
  },
};
</script>

<style lang="css" scoped>
	.header__container {
		display: flex;
		flex-direction: column;
		margin-top: 43px;
		margin-bottom: 30px;
	}
	.nav {
		display: flex;
		justify-content: space-between;
		margin-bottom: 33px;
	}
	.nav__list {
		display: flex;
		gap: 50px;
	}
	.nav__link {
		font-size: 14px;
		line-height: 19px;
		color: #000;
	}
	.nav__link:hover {
		color: #55B74C;
	}
	.nav__link:hover .nav__list {
		gap: 40px;
	}
	.user-account {
		display: flex;
		align-items: center;
	}
	.user-account p {
		margin-right: 10px;
		color: #55B74C;
	}
	.user-account p:hover {
		margin-right: 10px;
		color: #000;
	}
	.header__row {
		display: flex;
		justify-content: space-between;
		align-items: center;
		line-height: 19px;
		color: #898989;
	}
	.logo {
		margin-right: 235px;
	}
	.address {
		margin-right: 98px;
		display: flex;
		flex-direction: column;
		gap: 3px;
	}
	.address span {
		font-weight: 500;
		font-size: 18px;
		line-height: 25px;
		color: #000000;
	}
	.tel {
		position: relative;
		margin-right: 268px;
		display: flex;
		flex-direction: column;
		gap: 3px;
	}
	.tel a img {
		position: absolute;
		top: 24px;
		left: 0;
	}
	.tel a {
		padding-left: 28px;
		font-weight: 500;
		font-size: 18px;
		line-height: 25px;
		color: #55B74C;
	}
	.tools {
		position: relative;
		display: flex;
		align-items: center;
		gap: 20px;
	}
	.header__iput {
		width: 120%;
		position: absolute;
		padding: 4px 10px;
		font-size: 13px;
		line-height: 120%;
		right: 145px;
		top: -10%;
		opacity: 0;
		transition: 0.3s;
		visibility: hidden;
	}
	.visibility {
		visibility: visible;
		opacity: 1;
		top: 2px;
		transition: 0.3s;
	}

	@media (max-width: 1240px) {
    .logo {
    	margin-right: 100px;
    }
    .tel {
    	margin-right: 65px;
    }
    .menu__link {
    	font-size: 14px;
    }
  }
  @media (max-width: 1064px) {
  	.nav__list {
  		gap: 25px;
  	}
  	.nav__link {
  		font-size: 12px;
  	}
  	.logo {
  		margin-right: 0px;
  		max-width: 150px;
  	}
  	.logo img {
  		width: 100%;
  	}
  	.address {
  		margin-right: 0px;
  	}
  	.tel {
  		margin-right: 0px;
  	}
  	.tel a {
  		font-size: 14px;
  	}
  }
  @media (max-width: 808px) {
  	.header__container {
  		margin-bottom: 15px;
  	}
  	.nav {
  		margin-bottom: 15px;
  	}
  	.nav__list {
  		gap: 15px;
  	}
  	.nav__link {
  		font-size: 11px;
  	}
  	.user-account p {
  		font-size: 11px;
  	}
  	.logo {
  		max-width: 120px;
  	}
  	.address {
  		gap: 0px;
  	}
  	.address p {
  		font-size: 11px;
  	}
  	.address span {
  		font-size: 15px;
  		line-height: 120%;
  	}
  	.tel a {
  		padding-left: 23px;
  	}
  	.tel p, .tel a {
  		font-size: 11px;
  		line-height: 150%;
  	}
  	.tel a img {
  		max-width: 18px;
  		top: 16px;
  	}
  	.tools {
  		gap: 15px;
  	}
  	.tools a img {
  		max-width: 22px;
  	}
  }
</style>
