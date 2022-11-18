<template>
   <div id="getFixed"  class=" logobar container-fluid  ">
        <div class="row logo-bijoux">
           
          <Logo v-for="(logo,index) in logos" :key="index" :id="logo.id" :titre="logo.titre" :image="logo.image" />

      </div>
     </div>
     <p class="gratuite">Livraison gratuite pour les commandes supérieures à 50 €</p>
     <div class=" container-flid texte-center divvideo ">
      <div class="row align-items-center">
        <div class="col-mx-12 col-ms-12 col-md-4 col-lg-4 ">
       <p class="coeur">FAITES-VOUS PLAISIR  </p> 
         <p  id ="coeur"  class="coeur">Nos sélections coup de coeur </p>
       </div>
       <div class=" col-mx-12 col-ms-12 col-md-4 col-lg-4">
      <video
         controls
         src="src/assets/WhatsApp Video 2022-10-30 at 10.49.26.mp4"
         autoplay
         loop
         muted
         >
      </video>
     
    </div>
     </div>
    </div>
      
</template>
<script>
import Logo from '@/components/Logo.vue'
export default {
  name: 'LogoBijoux',
  components: {
  Logo,
  },
  props: {

  },
  data(){
      return {
          logos:[
              {
                  id:1,
                  titre:'Collier',
                  image:'f1.png',
              },
              {
                  id:2,
                  titre:'B.d\'orielle',
                  image:'f2.png',
              },
              {
                  id:3,
                  titre:'Bracelet',
                  image:'f3.png',
              },
              {
                  id:4,
                  titre:'Bague',
                  image:'f4.png',
              },
              {
                  id:5,
                  titre:'B.cheville',
                  image:'f5.png',
              },
              {
                  id:6,
                  titre:'Montre',
                  image:'Montere.png',
              },
          ],
      }
  },
}
</script>

