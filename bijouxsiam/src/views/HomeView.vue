<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <Carousel />
    <LogoBijoux/>
    <div class=" divfieldset container-fluid">
          <div   class="row justify-content-center  ">
            
            <Product v-for="(product,index) in products" :key="index" :id="product.id" :titre="product.titre" :image="product.image"  />
        </div>
    </div>
    <Livraison />
  </div>
</template>

<script>
// @ is an alias to /src
import Carousel from '@/components/Carousel.vue'
import LogoBijoux from '@/components/LogoBijoux.vue'
import Product from '@/components/Product.vue'
import Livraison from '@/components/Livraison.vue'
import axios from 'axios'

export default {
  name: 'Home',
  components: {
    LogoBijoux,
    Carousel,
    Product,
    Livraison,
  },
  
  data(){
        return {
            products:[],
            errors: []
        }
  },
  // Fetches Details when the component is created.
  created() {
    axios.get(`http://localhost:8080/details.json`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.details = response.data.details
    })
    .catch(e => {
      this.errors.push(e)
    })
  }  
}
</script>