<template>
  <q-card class="card-container">
    <div class="card-name">
      <div style="width: 80px" class="flex items-center">
        <q-avatar
          rounded
          text-color="white"
          :class="!item.thumbnailImageUuid ? 'bg-black':''"
          style="width: 80px; height: 80px;border-radius:8px;overflow:hidden"

          > <img v-if="item.thumbnailImageUuid" :src="'https://ph-files.imgix.net/'+ item.thumbnailImageUuid" /> {{ item.name[0].toUpperCase() }}</q-avatar
        >
      </div>
      <div class="name-holder q-pl-md space-evenly">
        <div class="text-weight-bold flex space-between">
          <span class="ellipsis name-hl">{{ item.name }}</span>
          <q-rating
            :model-value="item?.review_rating"
            size="1em"
            color="orange"
            readonly
          />
        </div>
        <div class="text-xs text-grey ellipsis-2-lines">{{ item.tagline }}</div>
        <div class="card-tag row space-between">
      <div v-if="item.topics" class="chip-holder q-mt-md">
        <q-chip
          v-for="(topic, index) in getTopics(item.topics)"
          :key="index"
          class="bg-chip q-ma-none q-mr-sm"
          size="sm"
          :label="topic"
        />
      </div>
    </div>
      </div>
    </div>

    <!-- <div
      class="card-content q-px-md q-mb-xs ellipsis-3-lines"
      v-html="item.description || 'N/A'"
    ></div> -->
  </q-card>
</template>

<script>
import mixin from 'src/mixins/mixin.js';

export default {
  name: 'ProductCard',
  mixins: [mixin],
  props: {
    item: { type: Object },
  },
  methods: {
    getTopics(topics) {
      return topics.split(',');
    },
  },
};
</script>

<style>
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
.card-tag {
  width: 100%;
}
.card-content {
  width: 100%;
  font-size: 12px;
}
.name-hl {
  width: calc(100% - 80px);
  font-size: 18px;
}
.name-holder {
  width: calc(100% - 50px);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.card-name {
  width: 100%;
  height: auto;
  display: flex;
  flex-direction: row;
  padding: 16px;
}
.button-border {
  border: 1px solid #4e4e4e;
}
.text-xs {
  font-size: 14px;
}
</style>
