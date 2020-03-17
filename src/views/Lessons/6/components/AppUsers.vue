<template>
  <div>
    <slot v-if="state === 'loaded'" :data="data" :count="count"> </slot>
    <slot v-if="state === 'loading'" name="loading"></slot>
    <slot
      v-if="state === 'failed'"
      :error="error"
      name="error"
      :retry="retry"
    ></slot>
  </div>
</template>

<script>
const states = {
  idle: "idle",
  loading: "loading",
  loaded: "loaded",
  failed: "failed"
};

export default {
  props: {
    promise: {
      type: Promise,
      required: true
    }
  },

  computed: {
    hasData() {
      if (!this.data) return;
      return this.data.length > 0;
    },
    count() {
      if (!this.data) return;
      return this.data.results.length;
    }
  },

  data() {
    return {
      state: "idle",
      data: undefined,
      error: undefined,
      states
    };
  },

  watch: {
    promise: {
      handler(value) {
        this.load(value);
      },
      immediate: true
    }
  },
  methods: {
    retry() {
      this.load(this.promise);
    },
    async load(promise) {
      if (!promise) return;
      this.state = "loading";
      this.error = undefined;
      this.data = undefined;
      try {
        const response = await promise;
        const json = await response.json();
        this.state = "loaded";
        this.data = json;
        return response;
      } catch (error) {
        this.state = "failed";
        this.error = error;
        return error;
      }
    }
  }
};
</script>
