<template>
  <v-form v-model="isFormValid" class="dynamic-form">
    <v-container fluid>
      <component
        v-bind:is="formElement.type"
        v-bind:formElement="formElement"
        v-bind:key="formElement.key"
        v-for="formElement in formStructure"
      >
      </component>
    </v-container>
  </v-form>
</template>

<script lang="ts">
import Vue from 'vue';
import TextFieldWrapper from './TextField.wrapper.vue';
import SelectFieldWrapper from './SelectField.wrapper.vue';
import RadioGroupWrapper from './RadioGroup.wrapper.vue';

export default Vue.extend({
  name: 'DynamicForm',
  components: {
    textField: TextFieldWrapper,
    selectField: SelectFieldWrapper,
    radioGroup: RadioGroupWrapper,
  },
  props: {
    formStructure: {
      type: Array,
      required: true,
    },
  },
  data() {
    return {
      isFormValid: false,
    };
  },
});
</script>

<style lang="scss" scoped></style>
