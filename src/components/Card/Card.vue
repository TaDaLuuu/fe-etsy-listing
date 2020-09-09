<template>
  <div>
    <b-card-group deck>
      <b-card>
        <template v-slot:header class="card-filter-header">
          <h5 class="mb-0 text-filter">Filter</h5>
        </template>
        <b-row align-v="end">
          <b-col cols="4">
            <Input placeholder="Search" />
          </b-col>
          <b-col cols="4">
            <Select />
          </b-col>
          <b-col cols="4">
            <b-button href="#" variant="primary">Search</b-button>
          </b-col>
        </b-row>
      </b-card>
    </b-card-group>
  </div>
</template>

<script>
import Input from "../Input/Input.vue";
import Select from "../Input/Select.vue";
export default {
  components: {
    Input,
    Select,
  },
};
</script>
<style lang="scss" scoped>
.card-header {
  background-color: #edcfa9;
}
</style>
