<script setup>
const supabase = useSupabaseClient();
const email = ref("");
const password = ref(null);
async function signIn() {
  const { data, error } = await supabase.auth.signInWithPassword({
    email: email.value,
    password: password.value,
  });
  if (error) throw error;
}
const user = useSupabaseUser();
</script>
<template>
  <main>
    <h1 class="centeralign">Login</h1>
    <br><section class="centeralign">
      <label for="email">
        Email
        <input type="email" v-model="email" />
      </label>
      <label for="password">
        Password
        <input type="password" v-model="password" />
      </label>
      <br><br><br><button @click="signIn">Sign In with E-Mail</button>
    </section>
    <section>
      <h1>Active user information</h1>
      <p v-if="user">{{ user.email }}</p>
    </section>
  </main>
</template>