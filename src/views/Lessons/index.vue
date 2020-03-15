<template>
  <component :is="dynamic" />
</template>

<script>
export default {
  data() {
    return {
      dynamic: () =>
        import(`@/views/Lessons/${this.$route.params.id}/index.vue`)
    };
  },
  watch: {
    "$route.params.id"(value) {
      console.log(value);
      this.dynamic = () => import(`@/views/Lessons/${value}/index.vue`);
    }
  }
};
</script>

<style></style>
