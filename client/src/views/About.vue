<template>
  <div id="app">
    <Header />>
    <PostComponent/>
  </div>
</template>

<script>
import PostComponent from '../components/PostComponent'
import Header from '../components/Header'

export default {
  name: 'App',
  components: {
    PostComponent,
    Header
  }
}
</script>

<style>
</style>
