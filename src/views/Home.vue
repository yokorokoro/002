<template>
 <v-main>
   <v-parallax dark src="../assets/works/background.jpg">
     <v-row align="center" justify="center">
       <v-col class="text-center" cols="12">
         <h1 class="display-1 font-weight-thin mb-4">PORTFOLIO</h1>
         <h4 class="subheading">my portfolio</h4>
       </v-col>
     </v-row>
   </v-parallax>
   <v-container class="pb-16">
     <h2 class="headline font-weight-bold text-center my-16">
       WORKS
     </h2>
     <ProductList></ProductList>
     <section class="section">
  <div class="inner">
    <div class="section-title-block">
      <h2 class="headline font-weight-bold text-center my-16">
        ABOUT
      </h2>
    </div>
    <v-row>
      <v-col cols="12" sm="12" md="4" lg="3"><img src="../assets/works/about.jpg" alt="" width="250"/></v-col>
      <v-col cols="12" sm="12" md="7" lg="9">
        <p class="text">
          テストテストテストテストテストテストテストテストテストテストテストテストテストテスト
          <br/>テストテストテストテストテストテストテストテストテストテストテストテストテストテスト
        </p>
      </v-col>
    </v-row>
  </div>
</section>
<section class="section">
  <div class="inner">
    <div class="section-title-block">
      <h2 class="headline font-weight-bold text-center my-16">
        CONTACT
      </h2>
      <p class="section-desc text-center">
        お問合わせは下記からご連絡をください。
      </p>
    </div>
    <div class="contact-wrapper">
      <div class="contact-list">
        <v-row class="text-center">
          <v-col>
            <v-btn href="" x-large="x-large" color="success" dark="dark">Extra large Button</v-btn>
          </v-col>
        </v-row>
      </div>
    </div>
  </div>
</section>
   </v-container>
 </v-main>
</template>
<script>
import ProductList from "../components/ProductList.vue";
export default {
 name: "Home",
 components: { ProductList },
};
</script>