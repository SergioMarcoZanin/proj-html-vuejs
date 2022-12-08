<template>
  <div>
    <HeaderComponent />
    <JumboComponent />
    <Main1Component />
    <Main2Component />
    <Main3Component />
    <Main4Component />
    <Main5Component />
    <Main6Component />
    <Main7Component />
    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import JumboComponent from './components/JumboComponent.vue';
import Main7Component from './components/Main7Component.vue';
import Main1Component from './components/Main1Component.vue';
import Main2Component from './components/Main2Component.vue';
import Main3Component from './components/Main3Component.vue';
import Main4Component from './components/Main4Component.vue';
import Main5Component from './components/Main5Component.vue';
import Main6Component from './components/Main6Component.vue';

export default {
  components: { HeaderComponent, Main1Component, FooterComponent, JumboComponent, Main2Component, Main3Component, Main4Component, Main5Component, Main6Component, Main7Component }
}
</script>

<style lang="scss" scoped>

</style>