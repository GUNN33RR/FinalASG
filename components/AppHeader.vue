<script setup>
const user = useSupabaseUser();
</script>
<template>
  <header>
    <nav>
    <NuxtLink to="login">Log In</NuxtLink>
      <NuxtLink to="signup">Sign Up</NuxtLink>
    </nav>
    <div class="buttons">
      <p v-if="user">{{ user.email }}</p>
      <Logout />
    </div>
  </header>
</template>

<style scoped>
header {
  background-color: black;
  color: white;
  display: flex;
  justify-content: space-between;
  padding: 1rem;
}
nav {
  display: flex;
  justify-content: space-around;
  gap: 2rem;
}
a,
div {
  color: white;
  text-decoration: none;
}
a:hover {
  color: silver;
}
.buttons {
  display: flex;
  gap: 8px;
}
.link {
  color: red;
  text-decoration: none;
  font-size: 1.5rem;
}
</style>