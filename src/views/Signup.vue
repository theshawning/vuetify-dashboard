<template>
  <v-container>
    <v-row>
      <v-col>
        <h1>Signup</h1>
        <v-form>
          <v-text-field label="Email" type="email" />
          <v-autocomplete label="Which browser do you use?" :items="browsers" />
          <v-file-input label="Attach profile picture" />
          <v-text-field 
            label="Birthday" 
            v-model="birthday" 
            readonly
          />
          <v-date-picker
            v-model="birthday"
          />
          <v-checkbox label="Agree to terms and conditions" />
          <v-btn type="submit" color="primary">Submit</v-btn>
        </v-form>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      browsers: [
        "Chrome",
        "Firefox",
        "Safari",
        "Edge",
        "Brave",
        "Internet Explorer",
        "Opera"
      ],
      birthday: ""
    };
  }
};
</script>

<style scoped>
</style>