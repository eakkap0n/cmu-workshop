<template>
  <div class="login">
    <h1>Login</h1>
    <form @submit.prevent="handleLogin">
      <div>
        <label for="username">Username:</label>
        <input type="text" id="username" v-model="username" required />
      </div>
      <div>
        <label for="password">Password:</label>
        <input type="password" id="password" v-model="password" required />
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'Login',
  setup() {
    const username = ref('');
    const password = ref('');

    const handleLogin = () => {
      // Handle login logic here
      console.log('Username:', username.value);
      console.log('Password:', password.value);
    };

    return {
      username,
      password,
      handleLogin,
    };
  },
});
</script>

<style scoped>
.login {
  max-width: 400px;
  margin: auto;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 5px;
}

.login h1 {
  text-align: center;
}

.login div {
  margin-bottom: 1em;
}

.login label {
  margin-bottom: .5em;
  color: #333333;
  display: block;
}

.login input {
  border: 1px solid #CCCCCC;
  padding: .5em;
  width: 100%;
  box-sizing: border-box;
}

.login button {
  padding: .5em;
  color: white;
  background-color: #007BFF;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  width: 100%;
}

.login button:hover {
  background-color: #0056b3;
}
</style>