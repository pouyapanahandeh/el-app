<template>
  <div class="row full-width">
    <div class="col-12 col-md-3">
      <q-card class="my-card q-ma-md">
        <img
          class="q-pa-sm"
          src="https://cdn.quasar.dev/img/parallax2.jpg"
          style="border-radius: 12px;"
        />

        <q-list>
          <q-item class="q-my-md">
            <q-item-section>
              <q-item-label class="flex flex-center">
                <span class="text-h4 text-white" >Name</span>
              </q-item-label>
            </q-item-section>
          </q-item>

          <q-item class="q-mb-md">
            <q-item-section>
              <q-item-label class="flex flex-center">
                <q-chip color="red" text-color="white">
                  In training
                </q-chip>
              </q-item-label>
            </q-item-section>
          </q-item>
        </q-list>
      </q-card>
    </div>
  </div>
</template>
<style>
.my-card {
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
</style>
