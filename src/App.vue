<template>
  <div>
    <HeaderComponent />
    <JumboComponent />
    <FeaturesCouresComponent />
    <CoursesComponent />
    <PriceCoursesComponent />
    <VideoYoutubeComponent />
    <CityCoursesComponent />
    <PeopleComponent />
    <NewslettersComponent />
    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import NewslettersComponent from './components/NewslettersComponent.vue';
import FeaturesCouresComponent from './components/FeaturesCouresComponent.vue';
import CoursesComponent from './components/CoursesComponent.vue';
import PriceCoursesComponent from './components/PriceCoursesComponent.vue';
import VideoYoutubeComponent from './components/VideoYoutubeComponent.vue';
import CityCoursesComponent from './components/CityCoursesComponent.vue';
import PeopleComponent from './components/PeopleComponent.vue';

export default {
  components: { HeaderComponent, FeaturesCouresComponent, FooterComponent, JumboComponent, CoursesComponent, PriceCoursesComponent, VideoYoutubeComponent, CityCoursesComponent, PeopleComponent, NewslettersComponent, }
}
</script>

<style lang="scss" scoped>

</style>