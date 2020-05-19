<script lang="ts">
import { defineComponent, computed } from "vue";

export default defineComponent({
  props: {
    msg: { type: String, required: true },
  },
  setup(props) {
    const uppercasedMsg = computed(() => props.msg.toUpperCase());

    return {
      uppercasedMsg,
    };
  },
});
</script>

<template>
  <div>
    <h1>{{ uppercasedMsg }}</h1>
  </div>
</template>
