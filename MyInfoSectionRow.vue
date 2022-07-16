<template>
  <div class="my-info-section-row__body">
    <my-info-section-card v-for="card in cards" :key="card.id" :card='card'></my-info-section-card>
    <my-info-section-card-two v-for="card in cardsTwo" :key="card.id" :card='card'></my-info-section-card-two>
  </div>
</template>

<script>
  import MyInfoSectionCard from '@/components/MyInfoSectionCard.vue'
  import MyInfoSectionCardTwo from '@/components/MyInfoSectionCardTwo.vue'

export default {

  components: {
    MyInfoSectionCard, MyInfoSectionCardTwo,
  },

  name: 'my-info-section-row',

  props: {
    cards: {
      type: Array,
      required: false,
      default: null,
    },
    cardsTwo: {
      type: Array,
      required: false,
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
  .my-info-section-row__body {
    display: flex;
    gap: 30px;
    margin-bottom: 75px;
  }
  .my-info-section-row__body:last-child {
    margin-bottom: 0;
  }
  @media (max-width: 1064px) {
    .my-info-section-row__body {
      margin-bottom: 30px;
    }
  }
  @media (max-width: 808px) {
    .my-info-section-row__body {
      gap: 20px;
      flex-wrap: wrap;
      align-items: center;
      justify-content: center;
    }
  }
</style>
