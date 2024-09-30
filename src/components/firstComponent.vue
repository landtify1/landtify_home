<template>
  <!-- <div class="q-pa-md">
    <q-layout view="lHh lpr lFf" container style="height: 400px" class="shadow-2 rounded-borders"> -->
  <!-- <q-header elevated>
    <q-toolbar>
      <q-avatar>
        <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
      </q-avatar>

      <q-toolbar-title> Quasar Framework </q-toolbar-title>

      <q-btn flat round dense icon="whatshot" />
    </q-toolbar>
  </q-header> -->

  <q-page-container :style="backgroundStyle" class="fullscreen-background">
    <!-- <q-page-container class="fullscreen-background"> -->
    <!-- <q-page padding> -->
    <div class="">
      <!-- <div class="gt-sm"> -->
      <div class="q-pt-xl">
        <div class="row">
          <div class="col-1 offset-1 q-mr-lg">
            <img
              src="~/assets/landtify_full.png"
              alt="logo"
              style="width: 210px; height: 74px"
            />
          </div>
          <!-- <div class="col-1 offset-8">
            <q-btn color="primary" label="Sign up" @click="goToSignup()" />
          </div> -->
        </div>
      </div>
      <!-- </div> -->
      <div class="q-mt-xl">
        <div class="row">
          <div class="col-5 offset-1">
            <div
              class="text-h6 q-pa-md caP"
              style="
                background-color: #69b44b;
                opacity: 75%;
                color: #ffffff;
                border-radius: 2%;
              "
            >
              Land is one of the most stable and rewarding investments you can
              make. Unlike other investments, land appreciates over time and
              requires minimal maintenance. Whether you're looking to build,
              farm, or simply hold it as a future asset, land investment offers
              security and growth potential.
            </div>
          </div>
          <!-- <div class="col-1 offset-4">
            <div class="row justify-end">
              <div class="column">
                <q-separator
                  vertical
                  color="primary"
                  style="width: 1px; height: 130px"
                  class="col-5 q-ml-sm q-mb-sm"
                />
                <img
                  class="col-1"
                  src="~/assets/facebook_vector.png"
                  alt="facebook"
                  style="width: 18px; height: 18px"
                />
                <img
                  class="col-1 q-mt-sm"
                  src="~/assets/instagram_vector.png"
                  alt="instagram"
                  style="width: 18px; height: 18px"
                />
                <q-separator
                  vertical
                  color="primary"
                  style="width: 1px; height: 130px"
                  class="col-5 q-ml-sm q-mt-sm"
                />
              </div>
            </div>
          </div> -->
        </div>
      </div>
      <div class="q-mt-xl">
        <div class="row">
          <div class="col-7 offset-1">
            <div class="row q-gutter-md q-ml-sm">
              <q-btn outline color="white" class="q-pa-md" @click="showNotif">
                <q-avatar size="24px">
                  <img src="~/assets/play_store.png" />
                </q-avatar>
                <div class="q-ml-sm">Play Store</div>
              </q-btn>
              <q-btn outline color="white" class="q-pa-md" @click="showNotif">
                <q-avatar size="24px">
                  <img src="~/assets/app_store.png" />
                </q-avatar>
                <div class="q-ml-sm">App Store</div>
              </q-btn>
            </div>
          </div>
        </div>
      </div>
      <div class="q-mt-xl q-pb-xl">
        <div class="row">
          <div class="col-4 offset-4">
            <div class="row">
              <q-separator class="col q-mt-sm" color="white" />
              <div class="q-mr-sm q-ml-sm text-white">landtify.com</div>
              <q-separator class="col q-mt-sm" color="white" />
            </div>
          </div>
        </div>
      </div>
      <!-- <div v-if="$q.platform.is.desktop" class="fullscreen-background">
        I'm only rendered on desktop!
      </div> -->

      <!-- <div v-if="$q.platform.is.mobile">I'm only rendered on mobile!</div> -->
      <!-- </q-page> -->
    </div>
  </q-page-container>
  <!-- </q-layout> -->
</template>
<script setup>
import { ref, onMounted } from "vue";
import { useQuasar } from "quasar";
// import { api } from "boot/axios";
import { useRouter } from "vue-router";
// import VueScrollTo from "vue-scrollto";
// import { useScrollTo } from "vue-scrollto";

const $q = useQuasar();
const $router = useRouter();
// const scrollTo = useScrollTo();

const targetSection = ref(null);
const showNotif = () => {
  $q.notify({
    message: "Under-construction",
    color: "primary",
  });
};
const goToScroll = (goto) => {
  targetSection.value = document.getElementById(goto);
  if (targetSection.value) {
    targetSection.value.scrollIntoView({ behavior: "smooth" });
  }
};

const goToSignin = () => {
  $router.push("/signin");
};

const goToSignup = () => {
  $router.push("/signup");
};

const images = [
  "/src/assets/land1.jpg",
  "/src/assets/land2.jpg",
  "/src/assets/land3.jpg",
  "/src/assets/land4.jpg",
  "/src/assets/land5.jpg",
  "/src/assets/land6.jpg",
];

const currentImageIndex = ref(0);
const backgroundStyle = ref({
  backgroundImage: `url(${images[currentImageIndex.value]})`,
});

const changeBackgroundImage = () => {
  currentImageIndex.value = (currentImageIndex.value + 1) % images.length;
  backgroundStyle.value = {
    backgroundImage: `url(${images[currentImageIndex.value]})`,
  };
};

onMounted(() => {
  setInterval(changeBackgroundImage, 5000); // Change image every 5 seconds
});
</script>

<style scoped>
/* .fullscreen-background {
  background-image: url(/src/assets/land1.jpg);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
} */
.fullscreen-background {
  width: 100vw;
  height: 100vh;
  background-size: cover;
  background-position: center;
  transition: background-image 1s ease-in-out;
}

.caP {
  font-family: "Balsamiq Sans", sans-serif;
  line-height: 50px;
  letter-spacing: 5%;
}

@media (max-width: 600px) {
  .caP {
    font-size: 10px; /* Adjust font size as needed */
    font-family: "Balsamiq Sans", sans-serif;
    line-height: 15px;
    letter-spacing: 0%;
  }
}
</style>
