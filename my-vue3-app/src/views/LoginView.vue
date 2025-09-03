<template>
  <div class="login-view">
    <h1>Login</h1>
    <Login />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Login from '@/components/Login.vue';

export default defineComponent({
  name: 'LoginView',
  components: {
    Login
  }
});
</script>

<style scoped>
.login-view {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
}
</style>