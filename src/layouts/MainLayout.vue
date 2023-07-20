<template>
  <q-layout view="lHh Lpr lFf">
    <q-header class="bg-white header">
      <q-toolbar>
        <q-toolbar-title class="text-black text-weight-bold">
          <q-img
            src="../assets/gmtlogo.png"
            :ratio="1"
            @click="$router.push('/')"
            style="
              height: 50px;
              width: 200px;
              border-radius: 10px;
              margin-right: 10px;
            "
          />
        </q-toolbar-title>
        <div class="row space-between">
          <!-- <q-btn
            label="Explore"
            class="toolbar-btn q-mr-md"
            unelevated
            no-caps
            to="/explore"
          ></q-btn> -->
          <q-btn
            label="About"
            class="toolbar-btn q-mr-md"
            unelevated
            to="/about"
            no-caps
          ></q-btn>

          <!-- <q-btn
            label="Contact Us"
            color="black"
            no-caps
            unelevated
            class="toolbar-btn q-ml-sm"
            filled
          ></q-btn> -->
        </div>
      </q-toolbar>
    </q-header>
    <list-product :showProductForm="showForm" @closeForm="closeForm" />
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import mixin from 'src/mixins/mixin.js';
import ListProduct from 'src/components/ListProduct.vue';
export default {
  components: { ListProduct },
  name: 'MainLayout',
  data() {
    return {
      showForm: false,
    };
  },
  mixins: [mixin],
  methods: {
    closeForm(event) {
      this.showForm = event;
    },
  },
};
</script>
<style scoped>
.header {
  height: 70px;
  display: flex;
  flex-direction: row;
  font-family: 'Poppins';
  border-bottom: 1px solid #e1e1e1;
}
</style>
