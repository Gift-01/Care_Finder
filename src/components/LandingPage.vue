<template>
  <div style="background-color: #e0e4ec">
    <div>
      <p>Find the nearest Hospital to you and make an appointment</p>
      <p>Discover your perfect care: find your Hospital, Anytime, Anywhere!</p>
      <button>Get started</button>
      <a href="#">Learn More</a>
    </div>
    <div>
      <img :src="Nurse" alt="Nurse and a patient" />
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Nurse from "../assets/NurseAndPatient.svg";

export default defineComponent({
  Nurse: Nurse as string,
});
</script>

<style></style>
