<template>
  <q-card class="card-container-v2" style="box-shadow: none">
    <div>
      <q-img
        src="https://picsum.photos/500/300"
        :ratio="1"
        style="height: 100px; width: 100%; border-radius: 6px"
      />
    </div>
    <div class="card-name">
      <div class="row">
        <div class="name-holder column space-evenly">
          <div class="text-weight-bold">Notion AI</div>
          <div class="text-xs text-grey">Notion</div>
        </div>
      </div>
      <div class="card-button">
        <q-rating :model-value="3" size="1em" color="orange" readonly />
      </div>
    </div>

    <div class="card-content-v2 q-mb-xs">
      Notion AI is a writing assistant that can help you write, brainstorm,
      edit, more..
    </div>

    <div class="card-tag q-pa-sm row space-between">
      <div class="chip-holder">
        <q-chip
          icon="alarm"
          class="bg-chip q-mr-sm"
          size="sm"
          label="Set alarm"
        />
        <q-chip
          icon="alarm"
          size="sm"
          class="bg-chip q-mr-sm"
          label="Set alarm"
        />
      </div>
    </div>
  </q-card>
</template>

<script>
import mixin from 'src/mixins/mixin.js';

export default {
  name: 'ProductCard',
  mixins: [mixin],
};
</script>

<style>
.card-container-v2 {
  height: auto;
  border-radius: 10px;
  overflow: hidden;
  font-family: 'Poppins';
  background: white;
}

.card-tag {
  width: 100%;
  top: 160px;
}
.card-content-v2 {
  width: 100%;
  font-size: 12px;
  padding: 0 16px;
  white-space: pre-line;
}

.card-name {
  height: auto;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
}
.button-border {
  border: 1px solid #4e4e4e;
}
.text-xs {
  font-size: 11px;
}
</style>
