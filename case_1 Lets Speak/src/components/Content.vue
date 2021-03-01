<template>
  <main class="page-main">
    <Slider />
    <SectionOffers />
    <SectionVideo />
    <SectionContacts />
  </main>
</template>

<script>
import Slider from "./Slider";
import SectionOffers from "./Sections/SectionOffers";
import SectionVideo from "./Sections/SectionVideo";
import SectionContacts from "./Sections/SectionContacts";
export default {
  components: { Slider, SectionOffers, SectionVideo, SectionContacts },
};
</script>

<style>
</style>