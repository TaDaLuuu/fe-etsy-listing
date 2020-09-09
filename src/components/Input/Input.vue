<template>
  <div>
    <label for="input-text" class="label">{{ label }}</label>
    <b-form-input v-model="text" :placeholder="placeholder"></b-form-input>
  </div>
</template>
<script>
export default {
  props: {
    label: {
      type: String,
      default: "",
    },
    placeholder: {
      type: String,
      default: "",
    },
  },
  data() {
    return {
      text: "",
    };
  },
};
</script>
<style lang="scss" scoped>
.label {
  display: block;
}
</style>