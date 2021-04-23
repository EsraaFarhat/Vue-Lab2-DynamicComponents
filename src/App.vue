<template>
  <div class="container">
    <div class="row">
      <ul class="list-inline col-12 text-center">
        <li class="list-inline-item"><a href="#" @click.prevent="targetComponent = 'HomeComponent'">Home</a></li>
        <li class="list-inline-item"><a href="#" @click.prevent="targetComponent = 'ContactComponent'">Contact</a></li>
        <li class="list-inline-item"><a href="#" @click.prevent="targetComponent = 'AboutComponent'">About</a></li>
      </ul>
    </div>
    <div class="row">
      <keep-alive>
        <component col-12 :is='targetComponent'></component>
      </keep-alive>
    </div>
  </div>
</template>

<script>
  import HomeComponent from './components/HomeComponent.vue'
  import ContactComponent from './components/ContactComponent.vue'
  import AboutComponent from './components/AboutComponent.vue'

export default {
  name: 'App',
  data(){
    return{
      targetComponent:'HomeComponent'
    }
  },
  components: {
    HomeComponent,
    ContactComponent,
    AboutComponent,
  }
}
</script>

<style>
li{
  font-size: 30px;
  margin: 20px;
}
</style>
