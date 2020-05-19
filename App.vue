<script lang="ts">
import { defineComponent } from "vue";
import HelloWorld from "./components/HelloWorld.vue";

export default defineComponent({
  components: {
    HelloWorld,
  },
});
</script>

<template>
  <div>
    <img alt="Vue logo" src="./logo.png" />
    <HelloWorld msg="hello world!" />
  </div>
</template>
