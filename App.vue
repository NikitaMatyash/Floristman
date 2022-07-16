<template>
  <my-header></my-header>
  <my-menu-row></my-menu-row>
  <my-section-image></my-section-image>
  <my-menu-section :cards="cards"></my-menu-section>
  <my-title>Акция</my-title>
  <my-slider></my-slider>
  <my-title>Заказать уникальный букет</my-title>
  <my-form-section></my-form-section>
  <my-info-section></my-info-section>
  <my-footer></my-footer>
</template>

<script>
  import MyHeader from '@/components/MyHeader.vue';
  import MyMenuRow from '@/components/MyMenuRow.vue';
  import MySectionImage from '@/components/MySectionImage.vue';
  import MyMenuSection from '@/components/MyMenuSection.vue';
  import MySlider from '@/components/MySlider.vue';
  import MyFormSection from '@/components/MyFormSection.vue';
  import MyInfoSection from '@/components/MyInfoSection.vue';
  import MyFooter from '@/components/MyFooter.vue';
  
export default {

  components: {
    MyHeader,
    MyMenuRow,
    MySectionImage,
    MyMenuSection,
    MySlider,
    MyFormSection,
    MyInfoSection,
    MyFooter,
    
  },

  name: 'App',

  data() {
    return {
      cards: [
        {id: 1, title: 'Цветы'},
        {id: 2, title: 'Подарки'},
        {id: 3, title: 'Фруктовые корзины'},
        {id: 4, title: 'Воздушные шарики'},
        {id: 5, title: 'Комнатные растения'},
        {id: 6, title: 'Сладости'},
        {id: 7, title: 'Услуги'},
        {id: 8, title: 'Аксессуары'},
      ],
    };
  },
};
</script>

<style lang="css">
  @import url('https://fonts.googleapis.com/css2?family=Inter&family=Manrope:wght@400;500;600;700&family=Roboto:wght@400;700&display=swap');

  * {
  padding: 0;
  margin: 0;
  border: 0; }

  *, *:before, *:after {
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    box-sizing: border-box; }

  :focus, :active {
    outline: none; }

  a:focus, a:active {
    outline: none; }

  nav, footer, header, aside {
    display: block; }

  html, body {
    height: 100%;
    width: 100%;
    font-size: 100%;
    line-height: 1;
    font-size: 14px;
    -ms-text-size-adjust: 100%;
    -moz-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%; }

  input, button, textarea {
    font-family: inherit; }

  input::-ms-clear {
    display: none; }

  button {
    cursor: pointer; }

  button::-moz-focus-inner {
    padding: 0;
    border: 0; }

  a, a:visited {
    text-decoration: none; }

  a:hover {
    text-decoration: none; }

  ul li {
    list-style: none; }

  img {
    vertical-align: top; }

  h1, h2, h3, h4, h5, h6 {
    font-family: inherit;
    font-weight: 400; }

  /*--------------------*/

  /*CONTAINER*/
  [class*="__container"] {
    max-width: 1240px;
    min-width: 1240px;
    margin: 0 auto;
    padding: 0 20px; }

  @media (max-width: 1240px) {
    [class*="__container"] {
      max-width: 1064px;
      min-width: 1064px;
    }
  }

  @media (max-width: 1064px) {
    [class*="__container"] {
      max-width: 808px;
      min-width: 808px;
    }
  }
  @media (max-width: 808px) {
    [class*="__container"] {
      max-width: 665px;
      min-width: 665px;
    }
  }
  @media (max-width: 665px) {
    [class*="__container"] {
      max-width: 465px;
      min-width: 465px;
    }
  }

  /*FONT*/
  body {
    font-family: 'Manrope', sans-serif;
    font-size: 14px;
    color: #000; }
</style>
