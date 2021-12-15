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
  data: () => ({
    sortYear: "全て",
    products: [
      {
        id: 1,
        name: "work1",
        image: "https://dummyimage.com/250x150/000/fff",
        year: "2020",
        category: "コーポレート",
        use: "html css JS",
      },
      {
        id: 2,
      name: "work2",
      image: "../assets/works/dummyimage.png",
      year: "2019",
      category: "LP",
      use: "Vue.js",
      info: "",
    }, {
      id: 3,
      name: "work3",
      image: "../assets/works/dummyimage.png",
      year: "2018",
      category: "ECサイト",
      use: "デザイン",
    }, {
      id: 4,
      name: "work4",
      image: "../assets/works/dummyimage.png",
      year: "2019",
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