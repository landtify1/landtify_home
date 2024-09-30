<template>
  <q-page-container class="fullscreen-background">
    <!-- <q-page padding> -->
    <!-- <div class="q-mt-sm">
      <div class="row">
        <div class="col-1 offset-2" style="color: #69b44b">
          <q-separator size="10px" color="primary" />
        </div>
      </div>
    </div> -->
    <div class="column" id="contact_us">
      <div class="col">
        <div class="row q-pt-xl q-pb-xl">
          <div class="col-10 offset-1" style="border: 1px solid #69b44b">
            <div class="row">
              <div
                class="col-12 col-md-4 q-pl-xl q-pt-xl"
                style="height: 615px"
              >
                <div class="column justify-between" style="height: 540px">
                  <div class="col q-pb-sm">
                    <!-- <div class="q-mt-xl"> -->
                    <div class="row">
                      <div class="col-5">
                        <div class="row" style="color: #69b44b">
                          <q-separator
                            color="primary"
                            class="col q-mt-sm q-mr-sm"
                          />
                          <div>CONTACT US</div>
                          <q-separator
                            color="primary"
                            class="col q-mt-sm q-ml-sm"
                          />
                        </div>
                      </div>
                      <!-- </div> -->
                    </div>
                    <div class="row">
                      <div
                        style="
                          font-family: Sam Sans;
                          font-size: 45px;
                          font-weight: 400;
                          line-height: 54px;
                        "
                      >
                        Let's&nbsp;<span style="color: #69b44b">Talk</span>
                      </div>
                    </div>
                    <div class="row">
                      <div style="font-family: Sam Sans">
                        Contact our team today about your query
                      </div>
                    </div>
                  </div>

                  <div class="col">
                    <!-- <div class="row"> -->
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
                          Proudly serving united state of america.
                        </p>
                      </div>
                      <div class="q-mt-md">
                        <p
                          class="col text-left"
                          style="
                            font-family: Poppins;
                            font-size: 18px;
                            font-weight: 700;
                            line-height: 21px;
                          "
                        >
                          CALL US
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
                          Phone: (904) 720-6883 <br />
                          <!-- <span style="color: #69b44b">Sunday: Closed</span> -->
                        </p>
                        <div class="q-mt-md">
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
                    <!-- </div> -->
                  </div>
                </div>
              </div>
              <!-- <q-separator color="primary" vertical /> -->
              <div class="col-12 col-md-8 q-pa-lg">
                <div class="row q-pt-md">
                  <div class="col-12 col-md-6 q-pl-md">
                    <q-input
                      required
                      class=""
                      v-model="first_name"
                      outlined
                      type="text"
                      hint="First Name"
                      label="Your First Name"
                    />
                  </div>
                  <div class="col-12 col-md-6 q-pl-md">
                    <q-input
                      required
                      class=""
                      v-model="last_name"
                      outlined
                      type="text"
                      hint="Last Name"
                      label="Your Last Name"
                    />
                  </div>
                </div>
                <div class="row q-pt-md">
                  <div class="col-12 col-md-6 q-pl-md">
                    <q-input
                      required
                      class=""
                      v-model="phone_number"
                      outlined
                      type="number"
                      label="+123 456 7890"
                      hint="Phone Number"
                    />
                  </div>
                  <div class="col-12 col-md-6 q-pl-md">
                    <q-input
                      required
                      class=""
                      v-model="email"
                      outlined
                      type="email"
                      label="johndoe@email.com"
                      hint="Email"
                    />
                  </div>
                </div>
                <div class="row q-pt-md">
                  <div class="col-12 col-md-12 q-pl-md">
                    <q-input
                      outlined
                      type="textarea"
                      v-model="message"
                      required
                      hint="Message "
                      label="Type Here"
                    />
                  </div>
                </div>
                <div class="row q-pt-md">
                  <!-- <div class="col-12 col-md-12 q-pl-md">
                    <q-input outlined type="textarea" v-model="message" hint="Message " label="Type Here" />
                  </div> -->
                  <q-btn
                    class="q-ml-md"
                    text-color="white"
                    style="
                      background-color: #69b44b;
                      border-radius: 8px;
                      width: 153px;
                      height: 55px;
                    "
                    label="SUBMIT"
                    :loading="loading"
                    @click="validatePost()"
                  >
                    <template v-slot:loading>
                      <q-spinner-hourglass class="on-left" />
                      Loading...
                    </template>
                  </q-btn>
                </div>
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
import { ref, onMounted } from "vue";
import { useQuasar } from "quasar";
// import services from "/src/json/services.json";
import { api } from "boot/axios";
// import { useRetailStore } from "src/stores/retail_store";

// const useStore = useRetailStore();

const $q = useQuasar();
const loading = ref(false);
const first_name = ref("");
const last_name = ref("");
const phone_number = ref("");
const email = ref("");
const message = ref("");
const serviceData = ref([]);

const validatePost = () => {
  if (first_name.value.length == 0) {
    $q.notify({
      color: "negative",
      message: "Please type something in First Name",
    });
  } else if (last_name.value.length == 0) {
    $q.notify({
      color: "negative",
      message: "Please type something in Last Name",
    });
  } else if (email.value.length == 0) {
    $q.notify({
      color: "negative",
      message: "Please type something in Email",
    });
  } else if (phone_number.value.length == 0) {
    $q.notify({
      color: "negative",
      message: "Please type something in Phone Number",
    });
  } else if (message.value.length == 0) {
    $q.notify({
      color: "negative",
      message: "Please type something in Message",
    });
  } else {
    postContactUs();
  }
};

const postContactUs = () => {
  // const token = useStore.getToken;
  loading.value = true;
  const formData = {
    firstname: first_name.value,
    lastname: last_name.value,
    email: email.value,
    phone: phone_number.value,
    message: message.value,
    platform: "Web-Home",
  };
  api
    .post("/contactus/home", formData, {
      headers: {
        Accept: "application/json",
      },
    })
    .then((response) => {
      console.log(response, "response");
      if (response.status == 201) {
        $q.notify({
          color: "green",
          position: "bottom",
          message: "Message Sent",
          caption: "Thank you!",
          icon: "check",
          timeout: "2000",
        });
        loading.value = false;
      } else if (response.data.success == false) {
        const _postContactUsFalseData = response.data;
        console.log(
          _postContactUsFalseData.value,
          "_postContactUsFalseData response!"
        );
        loading.value = fale;
      }
      first_name.value = "";
      last_name.value = "";
      phone_number.value = "";
      email.value = "";
      message.value = "";
    })
    // .catch(() => {
    .catch((e) => {
      console.log(e);
      loading.value = false;
    });
};

onMounted(() => {
  // const datas = services.services;
  // datas.forEach((data) => {
  //   serviceData.value.push(data.name);
  // });
  // serviceData.value.push("None of the Above");
  // console.log(serviceData.value, "contact serviceData");
  // console.log(datas, "contact datas");
  // console.log(useStore.getServiceListing, "main service listing");
  // const _data = useStore.getServiceListing;
  // console.log(new_data, "new_data");
});
</script>

<style scoped>
.fullscreen-background {
  /* background-image: url(/src/assets/hero_section.gif),
    linear-gradient(to right, #000000 21%, #000000 81%);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center; */
  /* height: 350px; */
}
</style>
