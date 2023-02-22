<template>
  <div class="fixed-container">
    <HeaderComponent />
    <IntroComponent />
    <DescComponent />
    <MapComponent />
    <MissionComponent />
    <AreasOfBusinessComponent />
    <CompensationComponent />
    <SliderComponent />
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import IntroComponent from "./components/IntroComponent.vue";
import DescComponent from "./components/DescComponent.vue";
import MapComponent from "./components/MapComponent.vue";
import MissionComponent from "./components/MissionComponent.vue";
import CompensationComponent from "./components/CompensationComponent.vue";
import SliderComponent from "./components/SliderComponent.vue";
import AreasOfBusinessComponent from "./components/AreasOfBusinessComponent.vue";

export default {
  components: {
    HeaderComponent,
    IntroComponent,
    DescComponent,
    AreasOfBusinessComponent,
    MapComponent,
    MissionComponent,
    CompensationComponent,
    SliderComponent,
  },
};
</script>

<style scoped></style>
