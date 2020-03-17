<template>
  <button class="button">
    {{ text }}<strong class="bold"> {{ bold }}</strong>
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String
    },
    bold: {
      type: String
    }
  }
};
</script>

<style>
.button {
  color: white;
  display: flex;
  align-items: center;
  padding: 0.375rem 0.75rem;
  min-height: 40px;
  border: none;
  background-color: #41b883;
  border-radius: 0.25rem;
  letter-spacing: 0.5px;
  font-size: 1rem;
  line-height: 1.125;
}

.bold {
  padding-left: 0.5em;
}
</style>
