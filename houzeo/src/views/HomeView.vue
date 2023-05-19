<template>
  <div class="home">
    <Navbar/>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from '../views/Navbar.vue'
export default {
  name: 'HomeView',
  components: {
    Navbar
  }
}
</script>
