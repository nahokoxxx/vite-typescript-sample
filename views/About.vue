<script lang="ts">
import { defineComponent } from "vue";
import { fetchMessage } from "../api/mock";

export default defineComponent({
  async setup() {
    const message = await fetchMessage();
    return { message };
  },
});
</script>

<template>
  <div class="container">
    {{ message }}
  </div>
</template>

<style scoped>
.container {
  margin: 0 auto;
  max-width: 1024px;
}
</style>
