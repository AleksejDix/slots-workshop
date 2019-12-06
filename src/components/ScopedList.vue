<template>
  <ul>
    <li v-for="item in list" :key="item.login.uuid">
      <slot :item="item" :promote="promote"></slot>
    </li>
  </ul>
</template>

<script>
export default {
  name: "HelloWorld",
  props: ["list", "fake", "output"],
  methods: {
    promote(name) {
      console.log(`${name} was promoted!`);
    }
  }
};
</script>
