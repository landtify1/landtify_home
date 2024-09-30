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
    <div class="column">
      <div class="col">
        <div class="row q-pt-xl">
          <div class="col-10 offset-1">
            <div class="row">
              <div class="col-12 col-md-4 q-mt-md">
                <div class="row">
                  <div class="column">
                    <div class="">
                      <p
                        class="col text-left"
                        style="
                          font-family: Poppins;
                          font-size: 18px;
                          font-weight: 700;
                          line-height: 21px;
                        "
                      >
                        OUR LOCATION
                      </p>
                      <p
                        class="col text-left q-mt-sm"
                        style="
                          font-family: Poppins;
                          font-size: 14px;
                          font-weight: 400;
                          line-height: 22.69px;
                        "
                      >
                        Proudly serving the United Stats of America.
                        <!-- , FL & the surrounding
                        areas. -->
                      </p>
                    </div>
                    <div class="q-mt-lg">
                      <p
                        class="col text-left"
                        style="
                          font-family: Poppins;
                          font-size: 18px;
                          font-weight: 700;
                          line-height: 21px;
                        "
                      >
                        HOURS OF OPERATION
                      </p>
                      <p
                        class="col text-left q-mt-sm"
                        style="
                          font-family: Poppins;
                          font-size: 14px;
                          font-weight: 400;
                          line-height: 22.69px;
                        "
                      >
                        Monday - Friday: 8:00 AM - 6:00 PM <br />
                        <!-- <span style="color: #02a0ac">Sunday: Closed</span> -->
                      </p>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-12 col-md-4 q-mt-md">
                <div class="row">
                  <div class="column">
                    <div class="">
                      <p
                        class="col text-left"
                        style="
                          font-family: Poppins;
                          font-size: 18px;
                          font-weight: 700;
                          line-height: 21px;
                        "
                      >
                        CONTACT US
                      </p>
                      <p
                        class="col text-left q-mt-sm"
                        style="
                          font-family: Poppins;
                          font-size: 14px;
                          font-weight: 400;
                          line-height: 22.69px;
                        "
                      >
                        Phone:  (904) 720-6883
                      </p>
                    </div>
                    <div class="q-mt-lg">
                      <p
                        class="col text-left"
                        style="
                          font-family: Poppins;
                          font-size: 18px;
                          font-weight: 700;
                          line-height: 21px;
                        "
                      >
                        SOCIALS
                      </p>
                      <div class="row q-gutter-sm">
                        <img
                          class="col-1"
                          src="~/assets/facebook.png"
                          alt="facebook"
                          style="width: 22.91px; height: 22.91px"
                        />
                        <img
                          class="col-1"
                          src="~/assets/instagram.png"
                          alt="instagram"
                          style="width: 22.91px; height: 22.91px"
                        />
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="col-12 col-md-4 q-mt-md">
                <div class="row">
                  <div class="column justify-around" style="height: 100px">
                    <div class="col-9">
                      <q-img
                        src="~/assets/landtify_full.png"
                        alt="fancy logo"
                      />
                    </div>
                    <!-- style="width: 250px; max-height: 150px" -->
                    <div class="col-3">
                      <p class="text-left">Land investment at ease...</p>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col">
        <q-separator size="2px" color="white" />
      </div>
      <div class="col q-pt-sm">
        <div class="row">
          <p
            style="
              font-family: Poppins;
              font-size: 14px;
              font-weight: 400;
              line-height: 22.69px;
            "
            class="col-5 offset-1 col-md-5"
          >
            All Rights Reserved | Landtify ©
            {{ year }}
          </p>
          <!-- <p
            style="
              font-family: Poppins;
              font-size: 14px;
              font-weight: 400;
              line-height: 22.69px;
            "
            class="col-5 col-md-5 text-center"
          > -->
          <!-- <span style="color: #02a0ac"
              >Terms of Service | Privacy Policy</span
            > -->
          <div
            class="col-5 col-md-5 text-center"
            align="right"
            style="cursor: pointer; text-decoration: underline; color: #69b44b"
          >
            <span @click="gotoPrivacy">Terms of Service </span>
            <span @click="gotoPrivacy">| Privacy Policy</span>
          </div>
          <!-- </p> -->
        </div>
      </div>
    </div>
  </q-page-container>
  <!-- </q-layout>
  </div> -->
</template>
<script setup>
// import { useQuasar } from "quasar";
import { useRouter } from "vue-router";

const $router = useRouter();

// const $q = useQuasar();

// $q.platform.is.mobile

const date_ = new Date();
const year = date_.getFullYear();

const gotoPrivacy = () => {
  $router.replace("/privacy");
};
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
