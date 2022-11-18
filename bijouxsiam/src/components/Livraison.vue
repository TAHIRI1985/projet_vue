<template>


<div class=" container">
          <div class="livraison row">
          <span class="col">
            <img src="css/images/icons8-livraison-de-nourriture-100 (2).png" alt="Livraison" >
            <p class="livrai">Livraison partout en France</p>
          </span>

          <span class="col">
             <img src="" alt="Paiment">
             <p class="paiement"> Paiement sécurisé 100%</p>
          </span>
          <span class="col">
            <img src="" alt="Echanges">
            <p class="Échanges">Échanges et remboursements</p>
         </span>
        </div>

        </div>   
</template>
<script>
export default {
  name: 'Livaisons',
  props: {
   
    titre:String,
    image:String,
  }
}
</script>