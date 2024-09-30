<template>
  <q-page-container class="fullscreen-background">
    <!-- <q-page padding> -->
    <!-- <div class="q-mt-sm">
      <div class="row">
        <div class="col-1 offset-2" style="color: #02a0ac">
          <q-separator size="10px" color="primary" />
        </div>
      </div>
    </div> -->
    <!-- <div class="column">
      <div class="col"> -->
    <div class="row q-pt-xl q-pb-xl" id="faqs">
      <div class="col-10 offset-1">
        <div class="row">
          <div class="col-2 offset-5">
            <div class="row" style="color: #69b44b">
              <q-separator color="primary" class="col q-mt-sm q-mr-sm" />
              FAQS
              <q-separator color="primary" class="col q-mt-sm q-ml-sm" />
            </div>
          </div>
          <!-- <div class="row"> -->
          <div
            class="col-6 offset-3"
            style="
              font-size: 38.5px;
              font-family: Sam Sans;
              font-weight: 400;
              line-height: 54px;
            "
          >
            <div class="row gt-md">FREQUENTLY ASKED QUESTIONS</div>
          </div>
          <div class="q-pa-md">
            <q-list>
              <div v-for="(faq, index) in serviceData" :key="faq[index]">
                <q-expansion-item
                  group="somegroup"
                  icon="fiber_manual_record"
                  :label="faq.question"
                  label-color="white"
                  default-opened
                  header-class="text-primary"
                  style="border: 1px solid #02a0ac; border-radius: 8px"
                  class="q-mb-md"
                >
                  <!-- label="First" -->
                  <q-card>
                    <q-card-section>
                      {{ faq.answer }}
                    </q-card-section>
                  </q-card>
                </q-expansion-item>

                <!-- <q-separator /> -->
              </div>
            </q-list>
          </div>
        </div>
      </div>
    </div>
    <!-- </div>
    </div> -->
  </q-page-container>
  <!-- </q-layout>
  </div> -->
</template>
<script setup>
import { ref, onMounted } from "vue";
// import { useQuasar } from "quasar";
import services from "/src/json/services.json";

// const $q = useQuasar();
const serviceData = ref([]);

onMounted(() => {
  serviceData.value = services.faqs;
  // console.log(serviceData.value, "serviceData");
});
</script>

<style scoped>
.fullscreen-background {
  /* background-image: url(/src/assets/new_images/hero_section.gif),
    linear-gradient(to right, #000000 21%, #000000 81%);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; */
  /* height: 350px; */
}
</style>
