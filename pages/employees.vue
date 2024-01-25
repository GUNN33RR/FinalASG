<script>
export default {
  async asyncData({ params }) {
    const { data, error } = await this.$supabase.from('employees').select('*');
    return { employees: data || [] };
  }
};
</script>

<template>
  <main>
    <h1>Employees</h1>
    <ul>
      <li v-for="employee in employees" :key="employee.EMPLOYEE_ID">
        <h3>Name: {{ employee.FIRST_NAME }} {{ employee.LAST_NAME }}</h3>
        <p>Email: {{ employee.EMAIL }}</p>
        <p>Phone: {{ employee.PHONE_NUMBER }}</p>
      </li>
    </ul>
  </main>
</template>
