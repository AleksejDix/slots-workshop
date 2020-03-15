<template>
  <ul class="gallery">
    <slot></slot>
  </ul>
</template>

<style>
.gallery {
  display: flex;
  flex-wrap: wrap;
  list-style: none;
  margin: 0;
  padding: 0;
}
</style>
