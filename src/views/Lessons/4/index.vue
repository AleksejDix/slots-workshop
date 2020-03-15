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
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          width="24"
          height="24"
        >
          <path
            class="heroicon-ui"
            d="M13 5.41V17a1 1 0 0 1-2 0V5.41l-3.3 3.3a1 1 0 0 1-1.4-1.42l5-5a1 1 0 0 1 1.4 0l5 5a1 1 0 1 1-1.4 1.42L13 5.4zM3 17a1 1 0 0 1 2 0v3h14v-3a1 1 0 0 1 2 0v3a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-3z"
          />
        </svg>
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
import AppButton from "@/views/Lessons/4/components/AppButton";
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
