<script setup>
const supabase = useSupabaseClient();

function logout() {
  try {
    const { error } = supabase.auth.signOut();
    if (error) throw error;
  } catch (error) {
    console.error(error);
  }
}
</script>
<template>
  <button @click="logout">Log Out</button>
</template>

<style scoped>
button {
  height: 32px;
  background-color: #8484d3;
  color: white;
}
</style>