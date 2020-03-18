<template>
  <div>
    <h1>Conditional wrapper</h1>
    <AppButton>
      buy <strong>now</strong>
      <template #second>
        only 3 Tickets left
      </template>
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
