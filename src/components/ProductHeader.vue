
<template>
  <v-flex align-end="align-end">
    <v-col class="px-0" cols="12" sm="6">
      <v-select :items="items" label="ここで作成年度：絞り込み" outlined="outlined" @change="sort" v-model="year"></v-select>
    </v-col>
  </v-flex>
</template>
<script>/* ソート機能 */
  export default {
    name: "ProductHeader",
    props: ["sortYear"],
    data: () => (
      {
        items: [
          "全て", "2020", "2019", "2018"
        ],
        year: "全て"
      }
    ),
    methods: {
      sort: function () {
        this.$emit("sortYearChange", this.year);
      }
    }
  };
</script>