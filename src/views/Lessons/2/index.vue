<template>
  <div class="owl-y">
    <h1>Named Slots</h1>
    <AppButton>
      <template #after>
        <Icon />
      </template>
      upload
    </AppButton>
    <AppButton>
      <template #before>
        <Icon />
      </template>
      upload
    </AppButton>
  </div>
</template>

<script>
import AppButton from "./components/AppButton";
export default {
  components: {
    AppButton
  }
};
</script>

<style></style>
