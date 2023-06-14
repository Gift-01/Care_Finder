<template>
  <NavBar />
  <div>Thanks for adding a to the list of hospitals</div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";

export default defineComponent({
  name: "AddHospital",
  components: {
    NavBar,
  },
});
</script>
