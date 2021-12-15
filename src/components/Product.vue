<template>
  <v-col cols="12" sm="6" md="4" lg="4">
    <v-card class="mx-auto">
      <v-img class="white--text align-end" height="200px" src="https://dummyimage.com/250x150/000/fff">
        <v-card-title>{{ product.name }}</v-card-title>
      </v-img>
      <v-card-subtitle class="pb-0">{{ product.year }}</v-card-subtitle>
      <v-card-text class="text--primary">
        <div>{{ product.category }}</div>
        <div>{{ product.use }}</div>
        <div>{{ product.info }}</div>
      </v-card-text>
      <v-card-actions>
        <v-btn color="orange" text="text">
          LINK
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-col>
</template>
<script>
/* Productを受け取る設定 */
  export default {name: "Product", props: ["product"]};
</script>
<style></style>