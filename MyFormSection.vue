<template>
	<div class="my-form-section__container">
		<my-form action="#" class="form" id="form">
	    <div class="form__body">
	      <my-input class="input" placeholder="Ваше имя*"></my-input>
	      <my-input class="input" placeholder="Ваш телефон*"></my-input>
	      <my-text-area class="text-area" placeholder="Ваша идея*"></my-text-area>
	      <div class="form__buttons">
	      	<button class="btn-add">+ Прикрепить файл</button>
	      	<button class="btn-send">Отправить</button>
	      </div>
	    </div>
	    <div class="form__img">
	    	<img src="@/assets/form-img.png" alt="">
	    </div>
	  </my-form>
	</div>
</template>

<script>
export default {

  name: 'my-form-section',

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
	.my-form-section__container {
		margin-bottom: 75px;
	}
	.form {
    display: flex;
    padding: 45px;
  }
  .form__body {
    display: flex;
    flex-direction: column;
    margin-right: 30px;
  }
  .form__body input {
  	margin-bottom: 20px;
  }
  .form__img {
  	max-height: 457px;
		max-width: 390px;
		border-radius: 7px;
  }
  .form__img img {
  	width: 100%;
  }
  .input {
  	min-width: 689px;
  	min-height: 56px;
  	padding: 15px 20px;
  	font-size: 20px;
		line-height: 27px;
  }
  .input::-webkit-input-placeholder {
  	color: #898989;
  }
  .text-area {
  	min-height: 219px;
		min-width: 689px;
		max-height: 219px;
		max-width: 689px;
		padding: 10px 20px;
  	font-size: 20px;
		line-height: 27px;
		color: #000;
		margin-bottom: 23px;
  }
  .text-area::-webkit-input-placeholder {
  	color: #898989;
  }
  .form__buttons {
  	display: flex;
  	gap: 30px;
  }
  .btn-add {
  	min-width: 356px;
		max-height: 60px;
		min-height: 60px;
		background: none;
		border: 2px solid #55B74C;
		border-radius: 7px;
		font-weight: 700;
		font-size: 24px;
		line-height: 33px;
		color: #55B74C;
  }
  .btn-send {
  	min-width: 303px;
		max-height: 60px;
		min-height: 60px;
		background: #55B74C;
		border-radius: 7px;
		font-weight: 700;
		font-size: 24px;
		line-height: 33px;
		color: #FFFFFF;
  }
  @media (max-width: 1240px) {
  	.form {
  		justify-content: center;
  	}
  	.form__img {
  		display: none
  	}
  }
  @media (max-width: 1064px) {
  	.my-form-section__container {
			margin-bottom: 45px;
		}
  	.form {
  		padding: 20px
  	}
  	.form__body {
  		margin-right: 0;
  	}
  	.text-area {
  		min-height: 170px;
  	}
  	.form__buttons {
  		justify-content: center;
  	}
  	.btn-add, .btn-send {
  		font-size: 18px;
  		max-height: 50px;
  		min-height: 50px;
  	}
  	.btn-add {
  		min-width: 270px;
  	}
  	.btn-send {
  		min-width: 240px;
  	}
  }
  @media (max-width: 808px) {
  	.my-form-section__container {
			margin-bottom: 35px;
		}
		.form__body {
			align-items: center;
			width: 100%;
		}
		.input {
			width: 100%;
			min-width: 100%;
		}
		.text-area {
			min-width: 100%;
		}
  }
</style>
