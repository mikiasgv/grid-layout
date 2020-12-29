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
  },
};
</script>

<style lang="scss">
@import "@/assets/sass/main.scss";
</style>
