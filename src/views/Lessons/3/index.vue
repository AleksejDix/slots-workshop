<template>
  <div class="owl-y">
    <h1>Converting from the old syntax</h1>
    <AppButton>
      <template #after>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 24 24"
          width="24"
          height="24"
        >
          <path
            class="heroicon-ui"
            d="M13 5.41V17a1 1 0 0 1-2 0V5.41l-3.3 3.3a1 1 0 0 1-1.4-1.42l5-5a1 1 0 0 1 1.4 0l5 5a1 1 0 1 1-1.4 1.42L13 5.4zM3 17a1 1 0 0 1 2 0v3h14v-3a1 1 0 0 1 2 0v3a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-3z"
          />
        </svg>
      </template>
      upload
    </AppButton>

    <div class="prose">
      <p>Wrap every slot element with <code>template</code> tag</p>
      <p>
        Cut the <code>slot="before"</code> attribute and apply it to the
        <code>template</code>
      </p>
      <p>
        Replace <code>slot="before"</code> with
        <code>v-slot:before</code>
      </p>
      <p>
        If you prefer the short syntax, then replace
        <code>v-slot:before</code> with <code>#before</code>
      </p>

      <p>
        Final code should look something like this
      </p>
      <code v-html="example"> </code>
    </div>
  </div>
</template>

<script>
import AppButton from "@/views/Lessons/3/components/AppButton";
export default {
  components: {
    AppButton
  },
  data() {
    return {
      example: `<AppButton>
            <template #after>
              <AppIcon/>
            </template>
            upload
          </AppButton>`
    };
  }
};
</script>

<style></style>
