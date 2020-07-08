<template>
  <div>
    <v-card width="400" class="mx-auto mt-5">
      <v-card-title>
        <h1 class="display-1">Login</h1>
      </v-card-title>
      <v-card-text>
        <v-form>
          <v-text-field 
            label="username"
            prepend-icon="mdi-account-circle" 
          />
          <v-text-field 
            label="password" 
            :type="showPassword ? 'text' : 'password'" 
            prepend-icon="mdi-lock"
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
            @click:append="showPassword = !showPassword"
          />
        </v-form>
      </v-card-text>
      <v-divider />
      <v-card-actions class="mt-1 mb-1">
        <v-btn color="green" dark>Register</v-btn>
        <v-spacer />
        <v-btn color="blue" dark>Login</v-btn>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showPassword: false
    };
  }
};
</script>

<style scoped>
</style>