<script setup>
// Fetch the data from a server route
const { data } = await useFetch("/api/employees", {
  headers: useRequestHeaders(["cookie"]),
});
const employees = data.value.employees;
</script>
<template>
  <main>
    <header>
    <h1 class="centeralign">Employees</h1>
  </header>
  <div>
   <ul>
      <li v-for="employee in employees" :key="employee.EMPLOYEE_ID">
        <h3>{{ employee.FIRST_NAME }} {{ employee.LAST_NAME }}:</h3>
        <p>Email: {{ employee.EMAIL }}</p>
        <p>Phone: {{ employee.PHONE_NUMBER }}</p>
      </li>
      </ul>
  </div>
  </main>
</template>