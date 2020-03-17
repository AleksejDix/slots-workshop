<template>
  <div class="owl-y">
    <h1>Dynamic Slot names</h1>
    <div class="owl-y">
      <label class="block" v-for="option in options" :key="option">
        <input type="radio" v-model="location" :value="option" />
        <span>{{ option }}</span>
      </label>
    </div>
    <AppButton>
      <template #[location]>
        <Icon />
      </template>
      upload
    </AppButton>

    <div class="prose">
      <p>
        You can make every names slot dynamic, by adding
        <code>v-slot[dynamic]</code>
        tag. Or use the shorthand Syntax <code>#[dynamic]</code>
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
