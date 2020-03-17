<template>
  <div class="owl-y">
    <h1>Fallback Content</h1>
    <AppButton />

    <div class="prose">
      <p>
        When you defined Slots in your components you can provide some fallback
        content
      </p>
    </div>
  </div>
</template>

<script>
import AppButton from "./components/AppButton";
export default {
  components: {
    AppButton
  },
  data() {
    return {
      location: "before",
      options: ["before", "after"]
    };
  }
};
</script>

<style>
.block {
  display: block;
}
</style>
