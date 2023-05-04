<template>
  <div class="container mx-auto">
    <navbar/>
    <div class="flex mt-10 items-center justify-center min-h-screen container mx-auto">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
        <card v-for="cat in kitties" :name="cat.name" :age="cat.age" :img="cat.img" :breed="cat.breed"/>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from './components/Nav/Navbar.vue'
import Card from './components/Cards/Card.vue'

export default {

  name: 'App',
  components: {
    Navbar,
    Card,
  },
  data(){
    return{
      kitties: this.getKitties()
    }
  },

  methods:{
    async getKitties(){
      let res = await fetch('kitties.json')
      let data = await res.json()
      this.kitties = data
  }
  }
}
</script>

