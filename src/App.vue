<template>
  <Sidebar />
  <Header />
  <Realtors />
  <Features />
  <Story />
  <StoryContent />
  <Homes />
  <Gallery />
  <Footer />
  <Levies/>
</template>

<script>
import Sidebar from "./components/SidebarComponent.vue";
import Header from "./components/HeaderComponent.vue";
import Realtors from "./components/RealtorsComponent.vue";
import Features from "./components/FeaturesComponent.vue";
import Story from "./components/StoryComponent.vue";
import StoryContent from "./components/StoryContentComponent.vue";
import Homes from "./components/HomesComponent.vue";
import Gallery from "./components/GalleryComponent.vue";
import Footer from "./components/FooterComponent.vue";
import Levies from "./components/LevisComponent.vue";

export default {
  name: "App",
  components: {
    Header,
    Sidebar,
    Realtors,
    Features,
    Story,
    StoryContent,
    Homes,
    Gallery,
    Footer,
    Levies
  },
};
</script>

<style lang="scss">
@import "@/assets/sass/main.scss";
</style>
