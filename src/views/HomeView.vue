<template>
  <div>
    <Navbar/>
    <ImageSection/>
    <RealStories/>
    <Footer/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '../views/Navbar.vue'
import ImageSection from '../views/ImageSection.vue'
import RealStories from '../views/RealStories.vue'
import Footer from '../views/Footer.vue'


export default {
  name: 'HomeView',
  components: {
    Navbar,
    ImageSection,
    RealStories,
    Footer
  }
}
</script>
