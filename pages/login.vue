<template>
  <div class="outer">
    <h1>Login</h1>
    <input type="text" v-model="username" placeholder="Email or Username" required /><br />
    <input type="password" v-model="password" placeholder="Password" required /><br />
    <button @click="handleLogin">Login</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    handleLogin() {
      alert(`Username: ${this.username}, Password: ${this.password}`);
    }
  }
};
</script>

<style scoped>
.outer {
  background-color: #294350;
  border-radius: 10px;
  padding: 80px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  color: #ffffff;
  max-width: 400px;
  width: 100%;
  text-align: center;
}
h1 {
  margin-bottom: 20px;
}
input {
  width: calc(100% - 20px);
  border: none;
  border-radius: 5px;
  padding: 10px;
  margin-bottom: 20px;
}
input[type="text"],
input[type="password"] {
  background-color: #ffffff;
  color: #294350;
}
button {
  background-color: #832324;
  color: #ffffff;
  border: none;
  border-radius: 5px;
  padding: 10px 20px;
  cursor: pointer;
  font-size: 16px;
  transition: background-color 0.3s;
}
button:hover {
  background-color: #a73737;
}
</style>
