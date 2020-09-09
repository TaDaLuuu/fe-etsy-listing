<template>
  <div class="overflow-auto mt-4">
    <b-row>
      <b-col cols="6">
        <b-pagination
          v-model="currentPage"
          :total-rows="rows"
          :per-page="perPage"
          aria-controls="my-table"
        ></b-pagination>
      </b-col>
      <b-col cols="2" offset="4">
        <dropdown />
      </b-col>
    </b-row>

    <b-table id="my-table" :items="items" :per-page="perPage" :current-page="currentPage" small></b-table>
  </div>
</template>

<script>
import Dropdown from "../Dropdown/Dropdown.vue";
export default {
  components: {
    Dropdown,
  },
  props: {
    currentPage: {
      default: 1,
      type: Number,
    },
    rows: {
      default: 1,
      type: Number,
    },
    perPage: {
      default: 1,
      type: Number,
    },
    items: {
      default: () => [],
      type: Array,
    },
  },
};
</script>