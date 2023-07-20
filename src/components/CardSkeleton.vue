<template>
  <q-card class="card-container">
    <q-item>
      <q-item-section>
        <q-item-label>
          <q-skeleton type="text" />
        </q-item-label>
        <q-item-label caption>
          <q-skeleton type="text" />
        </q-item-label>
      </q-item-section>
    </q-item>

    <q-card-actions class="row w-100 space-between">
      <q-skeleton type="QBtn" class="w-100" />
      <q-skeleton type="QBtn" class="w-100" />
    </q-card-actions>
    <q-item>
      <q-item-section>
        <q-item-label>
          <q-skeleton type="text" />
        </q-item-label>
        <q-item-label caption>
          <q-skeleton type="text" />
        </q-item-label>
      </q-item-section>
    </q-item>
  </q-card>
</template>

<script>
export default {
  name: 'CardSkeleton',
};
</script>

<style scoped>
.card-container {
  height: 200px;
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
</style>
