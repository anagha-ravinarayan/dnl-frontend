<template>
  <v-text-field
    :label="formElement.label"
    :placeholder="formElement.placeholder"
    :required="formElement.required"
  >
  </v-text-field>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'TextFieldWrapper',
  props: {
    formElement: {
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped></style>
