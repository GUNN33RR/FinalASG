<template>
  <main>
    <h1 class="centeralign">Welcome!</h1>
    <p>
      <a href="/login" class="button login-button">
        <button>Login</button>
      </a>
      <a href="/signup" class="button signup-button">
        <button>Sign up</button>
      </a>
      <a href="/departments" class="button departments-button">
        <button>Departments</button>
      </a>
      <a href="/employees" class="button employees-button">
        <button>Employees</button>
      </a>
    </p>
    <header>
      <nav>
      </nav>
    </header>
  </main>
</template>

<style>
.button {
  display: block; 
  width: 100%; 
  margin-bottom: 10px; 
  text-align: center;
  text-decoration: none;
}

.button button {
  width: 500px;
  padding: 10px;
  color: white;
  background-color: black;
  border: none;
  border-radius: 10px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.button button:hover {
  background-color: #333; 
}
</style>
