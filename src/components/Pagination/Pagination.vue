<template>
  <div class="overflow-auto">
    <div class="mt-3">
      <b-pagination
        v-model="currentPage"
        :total-rows="rows"
        :per-page="perPage"
        first-number
        last-number
      ></b-pagination>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    rows: {
      default: 1,
      perPage: 20,
      currentPage: 2,
    },
  },
};
</script>