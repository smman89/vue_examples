<template>
  <main class="page-main">
    <Slider />
    <SectionOffers />
    <SectionVideo />
    <SectionContacts />
  </main>
</template>

<script>
import Slider from './Slider'
import SectionOffers from './Sections/SectionOffers'
import SectionVideo from './Sections/SectionVideo'
import SectionContacts from './Sections/SectionContacts'
export default {
  components: { Slider, SectionOffers, SectionVideo, SectionContacts }
}
</script>

<style>
.page-main {
  grid-area: main;

  padding: 30px;

  display: grid;
  grid-template-columns: 3fr 1fr;
  grid-template-rows: 300px auto 1fr;
  grid-template-areas:
    'slider contacts'
    'offers contacts'
    'video contacts';
  grid-gap: 20px;
}
</style>