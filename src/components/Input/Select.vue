<template>
  <div>
    <b-form-select v-model="selected" :options="options"></b-form-select>
  </div>
</template>

<script>
export default {
  data() {
    return {
      selected: null,
      options: [
        { value: null, text: "Sort" },
        { value: "sale", text: "Sale" },
        { value: "views", text: "Views" },
        { value: "modified", text: "Last Modified" },
        { value: "creation", text: "Original Creation" },
      ],
    };
  },
};
</script>