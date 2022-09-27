<template>
  <div class="full-width">
    <div class="row flex flex-center">
      <div class="col-md-6 col-sm-10 col-xs-12">
        <q-input
          rounded
          outlined
          borderless
          hide-bottom-space
          class="full-width q-ma-md q-py-lg"
          id="gradiant"
          bg-color="white"
          v-model="text"
          placeholder="Search for ..."
        />
      </div>
    </div>
  </div>
</template>
<style scoped>
#gradiant {
  background: linear-gradient(
      207.53deg,
      #fa00ff 0%,
      #5690ff 25.52%,
      #fa00ff 48.96%,
      #22b0ff 74.48%,
      #e600eb 100%
    ),
    linear-gradient(0deg, #ffffff, #ffffff);
}
</style>>
