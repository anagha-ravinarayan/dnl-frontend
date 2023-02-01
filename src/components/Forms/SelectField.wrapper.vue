<template>
  <v-select
    :label="formElement.label"
    :placeholder="formElement.placeholder"
    :required="formElement.required"
    :items="formElement.items"
  >
  </v-select>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'SelectFieldWrapper',
  props: {
    formElement: {
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped></style>
