<template>
  <v-radio-group>
    <template v-slot:label>
      <div>
        {{ formElement.label }}
      </div>
    </template>
    <v-radio
      v-for="item in formElement.items"
      :key="item.value"
      :label="item.text"
      :placeholder="formElement.placeholder"
      :required="formElement.required"
    ></v-radio>
  </v-radio-group>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'RadioGroupWrapper',
  props: {
    formElement: {
      required: true,
    },
  },
});
</script>

<style lang="scss" scoped></style>
