<template>
  <div class="container mt-2">
    <div class="row">
    <div class="col-12">
      <!-- <h1>Header</h1> -->
      <HeaderComponent branch="Mansoura"/>
    </div>
    </div>
    <div class="row">
    <div class="col-4">
      <!-- <h1>Links</h1> -->
      <LinksComponent />
    </div>
    <div class="col-8">
      <!-- <h1>body</h1> -->
      <BodyComponent />
    </div>
    </div>
    <div class="row">
    <div class="col-12">
      <!-- <h1>Footer</h1> -->
      <FooterComponent />
    </div>
    </div>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue'
import LinksComponent from './components/LinksComponent.vue'
import BodyComponent from './components/BodyComponent.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    LinksComponent,
    BodyComponent,
    FooterComponent
  }
}
</script>

<style>

</style>
