<template>
  <div id="app">
    <ScopedList :list="users">
      <template #default="{ promote, item: {name: { first, last }} }">
        <button @click="promote(first)">{{ first + " " + last }}</button>
      </template>
    </ScopedList>
  </div>
</template>

<script>
import ScopedList from "./components/ScopedList.vue";

export default {
  components: {
    ScopedList
  },
  data() {
    return {
      users: []
    };
  },
  async mounted() {
    const response = await fetch(
      "https://randomuser.me/api/?page=3&results=10&seed=abc"
    );
    const json = await response.json();
    this.users = json.results;
  }
};
</script>
