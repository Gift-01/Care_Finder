<template>
  <div class="about">
    <NavBar />
    <h1>This is an about page</h1>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";
export default defineComponent({
  name: "AboutView",
  components: {
    NavBar,
  },
});
</script>
