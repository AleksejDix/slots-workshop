<template>
  <button class="button">
    <slot></slot>
    <div class="second" v-if="$slots.second">
      <slot name="second"></slot>
    </div>
  </button>
</template>

<style>
.button {
  color: white;
  align-items: center;
  padding: 0.375rem 0.75rem;
  min-height: 40px;
  border: none;
  background-color: #41b883;
  border-radius: 0.25rem;
  padding: 0.5 1rem;
  font-weight: bold;
  letter-spacing: 0.5px;
  font-size: 1.5rem;
  line-height: 1.125;
}

.second {
  display: block;
  font-size: 12px;
  min-height: 20px;
  margin-top: 0.5rem;
  border-top: 2px solid white;
  padding-top: 0.5rem;
}
</style>
