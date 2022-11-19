<template>
  <div class="home">
    <!--<img alt="Vue logo" src="../assets/logo.png">-->
    <Carousel/>
    <LogoBijoux/>
       <div class=" divfieldset container-fluid">
          <div   class="row justify-content-center  ">
            
            <Product v-for="(product,index) in products" 
                :key="index" :id="product.id"
               :description="product.description"   :prix="product.prix"
               :image="product.image"  :image2="product.image2" 
                :quantity="product.quantity" :count="product.count"/>
             
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
            errors: [],
            ajout:0
        }
  },
  computed: {
    totalProducts() {
      return this.products.reduce((sum, product) => {
        // sum += product.quantity
        // return sum
        return sum + product.quantity;
      }, 0);
    },
    totalPrix() {
      return this.products.reduce((total, product) => {
        return total + product.count * product.prix;
      }, 0);
    },
  },
  // Fetches Details when the component is created.
  created() {
    axios.get(`http://localhost:8080/products.json`)
    .then(response => {
      // JSON responses are automatically parsed.
      this.products = response.data.products
    })
    .catch(e => {
      this.errors.push(e)
    })
  }  
}
</script>
<style>
fieldset {
    color: #000;
    background-color: #fff;
    margin: 50px 50px;
    border-radius: 10px;
    box-shadow: 0px 0px 40px gray;
  }
  button {
    border: 0px;
    background-color: #fff;
  }
  
  #photo2 {
    z-index: 2;
    margin-top: -350px;
  
    height: 100%;
    width: 100%;
    padding-top: 0px;
  }
  #photo1 {
    cursor: pointer;
    height: 100%;
    width: 100%;
  }
  
  .f1 {
    background-size: 100% 100%;
  }
  #photo2 {
    visibility: hidden;
  }
  
  .f1:hover #photo2 {
    visibility: visible;
  }
  #voirplus {
    visibility: hidden;
    margin-bottom: 5px;
  }
  .non a:hover #voirplus {
    visibility: visible;
  }
  .non a {
    color: gray;
    text-decoration: none;
  }
  .non a:hover {
    color: gray;
  }
  article img {
    border-radius: 10px;
  }
  article {
    align-items: center;
  }
  .divfieldset {
    padding: 20px;
  }
  
  .ajouter {
    color: gray;
  }
  .ajouter :hover {
    color: gray;
  }
  
</style>