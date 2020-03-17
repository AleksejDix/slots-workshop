<template>
  <div class="owl-y">
    <h1>Converting from the old syntax</h1>
    <AppButton>
      <template #after>
        <Icon />
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
import AppButton from "./components/AppButton";
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
