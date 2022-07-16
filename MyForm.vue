<template>
	<form>
    <slot></slot>
  </form>
</template>

<script>
export default {

  name: 'my-form',

  data() {
    return {

    };
  },
};
</script>

<style lang="css" scoped>
  form {
    border: 1px solid #55B74C;
    border-radius: 8px;
  }
</style>
