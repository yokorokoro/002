<!-- ProductHeaderとProductをまとめるコンポーネント -->
<template>
  <div>
    <ProductHeader @sortYearChange="sortYearChanged($event)"></ProductHeader>
    <v-row>
      <product v-for="(product, key) in filterdList" :key="key" :product="product"></product>
    </v-row>
  </div>
</template>
<script >
import ProductHeader from "./ProductHeader.vue";
import Product from "./Product.vue";
export default {
  name: "ProductList",
  components: { ProductHeader, Product },
  data: () => (
    {/* 配列でデータを入れている */
    sortYear: "全て",
    products: [
      {
        id: 1,
        name: "●●会社さま",
    image_src:require('@/assets/works/img1.jpg'),
        year: "2020",
        category: "コーポレート",
        use: "html css JS",
      },
     
      {
        id: 2,
      name: "●●化学さま",
        image_src:require('@/assets/works/img2.jpg'),
      year: "2019",
      category: "LP",
      use: "Vue.js",
      info: "",
    }, {
      id: 3,
      name: "●●工芸さま",
    image_src:require('@/assets/works/img3.jpg'),      year: "2018",
      category: "ECサイト",
      use: "デザイン",
    }, {
      id: 4,
      name: "●●キャンペーンサイト",
    image_src:require('@/assets/works/img4.jpg'),      year: "2019",
      category: "LP",
      use: "Vue.js",
      info: "",
    }, ],
  }),  
  computed : {
  filterdList: function () {
    const newList = [];
    for (let i = 0; i < this.products.length; i ++) {
      if (this.sortYear === "2020" && this.products[i].year === "2020") {
        newList.push(this.products[i]);
      } else if (this.sortYear === "2019" && this.products[i].year === "2019") {
        newList.push(this.products[i]);
      } else if (this.sortYear === "2018" && this.products[i].year === "2018") {
        newList.push(this.products[i]);
      } else if (this.sortYear === "全て") {
        newList.push(this.products[i]);
      }
    }
    return newList;
  }
},
  methods: {
    sortYearChanged: function(year) {
      console.log(year);
      this.sortYear = year;
    },
  },

}; </script>