<template>
  <RouterLink to="/">Home</RouterLink>

  <RouterView />
</template>

<script>
import { RouterLink, RouterView } from "vue-router";

export default {
  name: "App",
};
</script>
