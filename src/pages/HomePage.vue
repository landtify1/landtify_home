<template>
  <q-layout>
    <firstComponent />
    <secondComponent />
    <thirdComponent />
    <!-- <fourthComponent />
    <fifthComponent /> -->
    <!-- <sixthComponent /> -->
    <seventhComponent />
    <eightComponent />
    <!-- <ninethComponent /> -->
    <tenthComponent />
  </q-layout>
</template>

<script setup>
import firstComponent from "../components/firstComponent.vue";
import secondComponent from "../components/secondComponent.vue";
import thirdComponent from "../components/thirdComponent.vue";
// import fourthComponent from "../components/fourthComponent.vue";
// import fifthComponent from "../components/fifthComponent.vue";
// import sixthComponent from "../components/sixthComponent.vue";
import seventhComponent from "../components/seventhComponent.vue";
import eightComponent from "../components/eightComponent.vue";
// import ninethComponent from "../components/ninethComponent.vue";
import tenthComponent from "../components/tenthComponent.vue";

defineOptions({
  name: "HomePage",
});
</script>
