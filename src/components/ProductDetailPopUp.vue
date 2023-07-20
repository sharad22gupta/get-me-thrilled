<template>
   <q-dialog v-model="showForm" class="backdrop-filter">
    <q-card class="form-container" style="border-radius:10px;max-width:1000px;width:80%">
      <div class="form-header">
        Product Details
      </div>
      <div>
      <div class="product-name">
      <div style="width: 80px" class="flex items-center">
        <q-avatar
          rounded
          text-color="white"
          class='bg-black'
          style="width: 80px; height: 80px;border-radius:8px;overflow:hidden"
          > {{ 'A' }}</q-avatar
        >
      </div>
      <div class="name-holder q-pl-md space-evenly">
        <div class="text-weight-bold flex space-between">
          <span class="ellipsis product-name-hl"> PhotoShop </span>
          <q-rating
            :model-value="5"
            size="1.5em"
            color="orange"
            readonly
          />
        </div>
        <div class="product-tag-line text-grey ellipsis-2-lines">Tag line tho yahi likhengay</div>
      </div>
    </div>
    <div class="product-card-tag q-mb-md">
          <div class="chip-holder">
            <q-chip
              :key="index"
              class="bg-chip q-ma-none q-mr-sm"
              size="sm"
              label="topic"
            />
            <q-chip
              :key="index"
              class="bg-chip q-ma-none q-mr-sm"
              size="sm"
              label="topic 2"
            />
          </div>
        </div>
    <div
      class="product-content"
    >
        What are some of the best project management tools available for remote teams
    What are some AI based of the most popular social media scheduling tools used by marketers
    Suggest some potential SaaS product ideas for businesses in the education sector.<br>
    What are some of the best project management tools available for remote teams
    What are some AI based of the most popular social media scheduling tools used by marketers
    Suggest some potential SaaS product ideas for businesses in the education sector
    </div>
      </div>
      <div class=" q-px-xl text-h6 q-mt-sm">
        Similar Products
      </div>
      <div class="similar-products">

         <product-card-v-2 class="smilar-product-card"  v-for="i in 10" :key="i"/>

      </div>
     </q-card>
    </q-dialog>
</template>

<script>
import ProductCardV2 from './ProductCardV2.vue'
export default {
  components: { ProductCardV2 },
  name: 'ProductDetailPopUp',
  data(){
    return{
      showForm: true
    }
  },
  props: {
    productDetails:{
      type: Object
    }
  }
}
</script>

<style>
.similar-products{
  padding: 20px 40px 40px 40px;
  overflow-x: scroll;
  overflow-y: hidden;
  white-space: nowrap;
}
.smilar-product-card{
  width: 400px;
  display: inline-block;
  margin-right: 20px;
}
.card-container {
  width: 100%;
  min-height: 100px;
  height: max-content;
  border-radius: 10px;
  overflow: hidden;
  font-family: 'Poppins';
  background: white;
  box-shadow: none;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
  /* box-shadow: 0 2px 4px rgba(45, 35, 66, 0.35),
    0 7px 13px -3px rgba(45, 35, 66, 0.25);
   */
  transition: transform 0.2s ease-out, box-shadow 0.2s ease-out;
}
.card-container:hover {
  transform: translate(5px,-5px);
   box-shadow: 0 2px 14px rgba(0, 0, 0, 0.35)

}
.product-card-tag {
  width: 100%;
  padding: 0 40px;
}
.product-content {
  width: 100%;
  font-size: 16px;
  padding: 0 40px 20px 40px;
}
.product-name-hl {
  width: calc(100% - 115px);
  font-size: 20px;
}
.name-holder {
  width: calc(100% - 50px);
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
}
.product-name {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: row;
  padding: 40px 40px 20px 40px;
}
.button-border {
  border: 1px solid #4e4e4e;
}
.product-tag-line {
  font-size: 16px;
}
.backdrop-filter{
  backdrop-filter: blur(5px);
}

</style>
