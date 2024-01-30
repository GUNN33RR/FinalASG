<script setup>
const {data} = await useFetch('/api/departments', {
  headers: useRequestHeaders(['cookie']),
});
const departments = data.value.departments;
</script>
<template>
  <main>
    <header>
      <h1 class="centeralign">Departments</h1>
    </header>
    <div>
      <ul>
        <li v-for="department in departments" :key="department.DEPARTMENT_ID">
        <h2>{{department.DEPARTMENT_NAME}}:</h2>
        <p>Department ID: {{ department.DEPARTMENT_ID }}</p>
        <p>Manager ID: {{ department.MANAGER_ID }}</p>
      </li>
      </ul>
    </div>
  </main>

</template>

