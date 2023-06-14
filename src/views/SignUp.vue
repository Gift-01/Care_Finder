<template>
  <div>
    <NavBar />
    <p>Signup details</p>
    <form @submit.prevent="submitForm" class="form-wrapper">
      <Input
        type="text"
        v-model="text"
        placeholder="Enter your Name"
        label="Full Name"
      />
      <Input
        label="Email"
        type="text"
        v-model="email"
        placeholder="Enter your Email"
        required
      />
      <Input
        label="password"
        type="password"
        v-model="password"
        placeholder="Password"
        required
      />
      <button
        type="submit"
        @click="submit"
        class="bg-gray-900 text-white w-[200px] m-2 rounded-lg p-1"
      >
        Create Account
      </button>
    </form>
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import NavBar from "@/components/NavBar.vue";
import Input from "@/components/InputField.vue";

export default defineComponent({
  components: {
    NavBar,
    Input,
  },
});
</script>
