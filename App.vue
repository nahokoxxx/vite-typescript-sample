<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({});
</script>

<template>
  <div>
    <header>
      <nav class="nav">
        <router-link class="link" :to="{ name: 'Home' }">Home</router-link>
        <router-link class="link" :to="{ name: 'About' }">About</router-link>
      </nav>
    </header>
    <main>
      <Suspense>
        <template #default>
          <router-view />
        </template>
        <template #fallback>
          loading...
        </template>
      </Suspense>
    </main>
  </div>
</template>

<style scoped>
.nav {
  margin-bottom: 2rem;
}

.link {
  font-weight: bold;
  color: #42b883;
}

.link + .link {
  margin-left: 1rem;
}
</style>
