<template>
  <div>
    <NavBar />
    <p>Welcome Back, you have been missed</p>
    <form @submit.prevent="" class="form-wrapper">
      <div class="flex flex-col">
        <Input
          label="Email"
          type="text"
          v-model="email"
          placeholder="Enter your Email"
          required
        />
        <Input
          label="Password"
          type="password"
          v-model="password"
          placeholder="password"
          required
        />
      </div>
      <button
        type="submit"
        class="bg-gray-900 text-white w-[300px] m-2 rounded-lg p-1"
      >
        Login
      </button>
      <p>or</p>
      <div class="flex-col mx-[80px]">
        <button class="bg-gray-900 text-white rounded-lg w-[300px] p-1 m-2">
          Sign in with Google
        </button>
        <button class="bg-gray-900 text-white w-[300px] m-2 rounded-lg p-1">
          Sign in facebook
        </button>
        <button class="bg-gray-900 text-white w-[300px] m-2 rounded-lg p-1">
          Sign in Apple
        </button>
        <button class="bg-gray-900 text-white w-[300px] m-2 rounded-lg p-1">
          Sign in Instagram
        </button>
      </div>
      <p>
        You don't have an account?
        <router-link to="/signUp" class="text-green-500">
          Create an account</router-link
        >
      </p>
    </form>
  </div>
</template>

<script lang="ts">
import NavBar from "@/components/NavBar.vue";
import Input from "@/components/InputField.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "LoginView",
  components: {
    NavBar,
    Input,
  },

  data() {
    return {
      email: "",
      password: "",
      error: "",
    };
  },
});
</script>

<style>
.form-wrapper {
  max-width: 500px;
  margin: 0 auto;
  padding: 20px;
  background-color: #f1f1f1;
  border-radius: 5px;
  box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.3);
}
</style>
