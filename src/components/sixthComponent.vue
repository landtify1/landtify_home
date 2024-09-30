<template>
  <q-page-container class="fullscreen-background" id="gallery">
    <!-- <q-page padding> -->
    <div class="q-pt-xl q-pb-xl">
      <div class="">
        <div class="row">
          <div class="col-8 offset-2">
            <div class="row justify-center">
              <div class="col-3">
                <q-separator size="5px" color="primary" />
              </div>
            </div>
            <p
              class="text-center"
              style="
                font-family: Sam Sans;
                font-size: 35px;
                font-weight: 400;
                letter-spacing: 0.05em;
              "
            >
              VIEW OUR&nbsp;<span style="color: #69b44b">CURRENT</span>
              AND&nbsp;<span style="color: #69b44b">PAST</span> DETAILING
              PROJECTS
            </p>
          </div>
        </div>
      </div>
      <div class="q-mt-sm">
        <div class="row">
          <div class="col-10 offset-1">
            <div class="row">
              <div class="col-12 col-md-4 q-pa-md">
                <q-img
                  src="~/assets/new_images/past1.png"
                  alt="6th com logo"
                  style="height: 510px"
                />
              </div>
              <div class="col-12 col-md-4 q-pa-md">
                <div class="column justify-between" style="height: 510px">
                  <div class="col">
                    <q-img
                      src="~/assets/new_images/past2.png"
                      alt="6th com logo"
                      style="height: 236px"
                    />
                  </div>
                  <div class="col">
                    <q-img
                      src="~/assets/new_images/past3.png"
                      alt="6th com logo"
                      style="height: 236px"
                    />
                  </div>
                </div>
              </div>
              <div class="col-12 col-md-4 q-pa-md">
                <q-img
                  src="~/assets/new_images/past4.png"
                  alt="6th com logo"
                  style="height: 510px"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page-container>
  <!-- </q-layout>
  </div> -->
</template>
<script setup>
import { ref } from "vue";
// import { useQuasar } from "quasar";

// const $q = useQuasar();
const gallery = ref(null);

// $q.platform.is.mobile
</script>

<style scoped>
.fullscreen-background {
  /* background-image: url(/src/assets/new_images/hero_section.gif),
    linear-gradient(to right, #000000 21%, #000000 81%);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; */
  /* height: 680px; */
}
</style>
