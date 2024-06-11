<script lang="ts">
import axios from "axios";

export default {
  components: {},
  data: () => ({
    username: "",
    email: "",
    birthdate: "",
  }),
  methods: {
    handleClick() {
      axios.post("http://localhost:3000/users/create", this.$data);
    },
  },
};
</script>

<template lang="pug">
  div.flex.flex-col.items-center.gap-2
    input.border.border-1.p-1.m-1(name="username" placeholder="username" v-model="username")
    input.border.border-1.p-1.m-1(name="username" placeholder="username" v-model="email")
    input.border.border-1.p-1.m-1(name="username" placeholder="username" v-model="birthdate")
    button.border.border-1.p-1(@click="handleClick") click
</template>
