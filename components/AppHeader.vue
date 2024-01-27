<template>
  <header>
    <div>
      <NuxtLink to="/">Home</NuxtLink>
    </div>
    <nav>
      <NuxtLink to="departments">Departments</NuxtLink>
      <NuxtLink to="employees">Employees</NuxtLink>
      <NuxtLink to="login">Log In</NuxtLink>
      <NuxtLink to="signup">Sign Up Page</NuxtLink>
    </nav>
  </header>
</template>

<style scoped>
header {
  background-color: black;
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
  color: red;
}
.buttons {
  display: flex;
  gap: 8px;
}
.link {
  color: blue;
  text-decoration: none;
  font-size: 1.5rem;
}
</style>