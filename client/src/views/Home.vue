<template>
  <div id="app">
    <Header />
    <Map />
    <Footer />
  </div>
</template>

<script>
import Header from "../components/Header"
import Map from "../components/Map"
import Footer from "../components/Footer"

export default {
  name: 'App',
  components: {
    Header,
    Map,
    Footer
  }
}
</script>

<style>

</style>
