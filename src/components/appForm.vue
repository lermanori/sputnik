<template>
  <v-card dark class="ma-5 pa-3">
    <form>
      <v-text-field
        v-model="name"
        v-validate="'required|max:10'"
        :counter="10"
        label="Name"
        data-vv-name="name"
        required
      ></v-text-field>
      <v-text-field
        v-model="email"
        v-validate="'required|email'"
        label="E-mail"
        data-vv-name="email"
        required
      ></v-text-field>
      <v-text-field v-model="mobile" label="mobile" data-vv-name="mobile" required></v-text-field>

      <v-checkbox
        v-model="outDoorSitting"
        v-validate="'required'"
        value="1"
        label="out-door sitting"
        data-vv-name="outDoorSitting"
        type="checkbox"
        required
      ></v-checkbox>

      <v-btn class="mr-4" @click="submit">submit</v-btn>
      <v-btn @click="clear">clear</v-btn>
    </form>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    mobile: "",
    name: "",
    email: "",
    outDoorSitting: null,
    dictionary: {}
  }),

  mounted() {},

  methods: {
    submit() {},
    clear() {
      this.name = "";
      this.email = "";
      this.select = null;
      this.checkbox = null;
    }
  }
};
</script>