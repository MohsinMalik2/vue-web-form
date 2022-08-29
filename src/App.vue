<template>
  <div class="container">
    <div class="col card">
      <div class="card-body">
        <h1>Vue Component</h1>
        <SignupForm />
      </div>
    </div>
  </div>
</template>

<script>
import SignupForm from "./components/SignupForm.vue";

export default {
  name: "App",
  components: { SignupForm },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
