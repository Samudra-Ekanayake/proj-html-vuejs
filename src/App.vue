<script>
import AppHeader from './components/AppHeader.vue'
import SectionTextImg from './components/SectionTextImg.vue';
import Carousel from './components/Carousel.vue';
import CardContainer from './components/CardContainer.vue';
import Behavior from './components/Behavior.vue';
import BestTutor from './components/BestTutor.vue';
import PageFooter from './components/PageFooter.vue'

export default {

  components: {
    AppHeader,
    SectionTextImg,
    Carousel,
    Behavior,
    CardContainer,
    BestTutor,
    PageFooter
  },

  data() {
    return {

    }
  },

  methods: {


  },

  mounted() {

  },

}
</script>

<template>

  <AppHeader />
  <SectionTextImg />
  <Carousel />
  <Behavior />
  <CardContainer />
  <BestTutor />
  <PageFooter />

</template>

<style scoped></style>
