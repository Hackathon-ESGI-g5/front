<template>

  <div class="flex flex-col w-56 m-auto my-4">
    <label class="font-semibold text-gray-700 text-left block mb-2">{{ label }}</label>
    <Field :key="name"
           :type="type"
           :name="name"
           :value="value"
           :required="required"
           :disabled="disabled"
           class="bg-grey"
    >
      <slot></slot>
    </Field>
  </div>


</template>

<script>
  import Field from './Field'
  export default {
    name: "FormGroup",
    components: {
      Field
    },
    props: ['type', 'label', 'name', 'value', 'required', 'disabled']
  }
</script>

<style scoped>

</style>
