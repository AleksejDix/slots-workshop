<template>
  <button class="button">
    <slot name="before">
      <svg
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 24 24"
        width="24"
        height="24"
      >
        <path
          class="heroicon-ui"
          d="M13 5.41V17a1 1 0 0 1-2 0V5.41l-3.3 3.3a1 1 0 0 1-1.4-1.42l5-5a1 1 0 0 1 1.4 0l5 5a1 1 0 1 1-1.4 1.42L13 5.4zM3 17a1 1 0 0 1 2 0v3h14v-3a1 1 0 0 1 2 0v3a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-3z"
        /></svg
    ></slot>
    <span class="button__text"><slot>Fallback Text</slot></span>
    <slot name="after"></slot>
  </button>
</template>

<style>
.button {
  color: white;
  display: flex;
  align-items: center;
  padding: 0.375rem 0.75rem;
  min-height: 40px;
  border: none;
  background-color: crimson;
  border-radius: 0.25rem;
}

.button__text {
  padding: 0 0.5rem;
  font-weight: bold;
  letter-spacing: 0.5px;
  font-size: 1rem;
  line-height: 1.125;
}
</style>
