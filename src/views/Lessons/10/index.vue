<template>
  <div class="owl-y">
    <h1>All features combined</h1>
    <AppUsers :promise="getUsers">
      <template #default="{data, count}">
        {{ count }}
        <ul class="userlist owl-y" v-if="data.results">
          <li v-for="user in data.results" :key="user.login.uuid">
            <div>
              <h1>
                {{ user.name.title }} {{ user.name.first }}
                {{ user.name.last }}
              </h1>
            </div>
          </li>
        </ul>
      </template>
      <template #loading>loading...</template>
      <template #error="{retry, error}">
        <pre>{{ error }}</pre>
        <AppButton @click="retry">retry</AppButton>
      </template>
    </AppUsers>
  </div>
</template>

<script>
import AppUsers from "./components/AppUsers";
import AppButton from "./components/AppButton";
export default {
  components: {
    AppButton,
    AppUsers
  },
  data() {
    return {
      getUsers: fetch("https://randomuser.me/api/?results=5")
    };
  }
};
</script>

<style>
.block {
  display: block;
}

.userlist {
  list-style: none;
  padding: 0;
  margin: 0;
}

.userlist > li {
  border: 1px solid gray;
  border-radius: 0.25rem;
  padding: 1rem;
}
</style>
