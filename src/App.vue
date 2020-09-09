<template>
  <div id="app">
    <h1 class="mb-5">GodGroup Listing Tool</h1>
    <b-form-group>
      <b-row align-v="end">
        <b-col cols="8" offset="1">
          <Input label="Nhập URL cần lấy thông tin" placeholder="Enter your URL" />
        </b-col>
        <b-col cols="2">
          <b-button variant="success" pill block>Get</b-button>
        </b-col>
      </b-row>
    </b-form-group>

    <table-horizontal :items="this.itemsHorizontal" />
    <card />

    <table-vertical :items="this.itemsVertical" :currentPage="1" :perPage="20" :rows="rows" />
  </div>
</template>
<script>
import Input from "./components/Input/Input.vue";
import TableVertical from "./components/Table/TableVertical.vue";
import TableHorizontal from "./components/Table/TableHorizontal.vue";
import Card from "./components/Card/Card.vue";
export default {
  name: "App",
  components: {
    Input,
    TableVertical,
    TableHorizontal,
    Card,
  },
  data() {
    return {
      itemsVertical: [
        { age: 40, first_name: "Dickerson", last_name: "Macdonald" },
        { age: 21, first_name: "Larsen", last_name: "Shaw" },
        { age: 89, first_name: "Geneva", last_name: "Wilson" },
        { age: 38, first_name: "Jami", last_name: "Carney" },
      ],
      itemsHorizontal: [
        { age: 40, first_name: "Dickerson", last_name: "Macdonald" },
      ],
    };
  },
  computed: {
    rows() {
      return this.itemsVertical.length;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  padding: 60px 20px;
}
</style>
