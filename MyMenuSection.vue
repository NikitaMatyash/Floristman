<template>
  <div class="my-menu-section__container">
    <div class="my-menu-section__body">
      <my-menu-section-item :card="card" v-for='card in cards' :key="card.id"></my-menu-section-item>
    </div>
  </div>
</template>

<script>
  import MyMenuSectionItem from "@/components/MyMenuSectionItem.vue"

export default {

  components: {
    MyMenuSectionItem,
  },

  props: {
    cards: {
      type: Array,
      required: true,
      default: null,
    },
  },

  name: 'my-menu-section',

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
  .my-menu-section__container {
    margin-bottom: 75px;
  }
  .my-menu-section__body {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 29px;
  }
  @media (max-width: 1064px) {
    .my-menu-section__container {
      margin-bottom: 45px;
    }
    .my-menu-section__body {
      justify-content: space-between;
      gap: 15px;
    }
  }
  @media (max-width: 808px) {
    .my-menu-section__container {
      margin-bottom: 35px;
    }
  }
</style>
