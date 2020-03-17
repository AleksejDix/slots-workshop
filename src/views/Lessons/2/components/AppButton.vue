<template>
  <button class="button">
    <slot name="before"></slot>
    <span class="button__text"><slot></slot></span>
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
  background-color: #41b883;
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
