<template>
  <div id="wrapper-main">
    <Navigation></Navigation>
    
    <div id="wrapper-content">
      <div class="wrapper-content-back"></div>
      <Header></Header>
      <router-view/>
    </div>
  </div>
</template>

<script>
import Navigation from './components/Navigation.vue'
import Header from './components/Header.vue'

export default {
  name: 'app',
  components: {
    Navigation,
    Header
  }
}
</script>