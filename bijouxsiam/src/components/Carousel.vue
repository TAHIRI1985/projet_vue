<template>


<div class="carosel container-fluid ">
          <div class="divcarosel  container-fluid ">
            <div
              id="carouselExampleDark"
              class="carousel carousel-dark slide "
              data-bs-ride="carousel"
              
            >
              <div class="carousel-indicators">
                <button
                  type="button"
                  data-bs-target="#carouselExampleDark"
                  data-bs-slide-to="0"
                  class="active"
                  aria-current="true"
                  aria-label="Slide 1"
                ></button>
                <button
                  type="button"
                  data-bs-target="#carouselExampleDark"
                  data-bs-slide-to="1"
                  aria-label="Slide 2"
                ></button>
                <button
                  type="button"
                  data-bs-target="#carouselExampleDark"
                  data-bs-slide-to="2"
                  aria-label="Slide 3"
                ></button>
              </div>

              <div class=" divcarousel carousel-inner">
                
                <Slide v-for="(slide,index) in slides" :key="index" :id="slide.id" :titre="slide.titre" :image="slide.image"  />
            

              </div>

              <button
                class="carousel-control-prev"
                type="button"
                data-bs-target="#carouselExampleDark"
                data-bs-slide="prev"
              >
                <span
                  class="carousel-control-prev-icon"
                  aria-hidden="true"
                ></span>
                <span class="visually-hidden">Previous</span>
              </button>
              <button
                class="carousel-control-next"
                type="button"
                data-bs-target="#carouselExampleDark"
                data-bs-slide="next"
              >
                <span
                  class="carousel-control-next-icon"
                  aria-hidden="true"
                ></span>
                <span class="visually-hidden">Next</span>
              </button>
            </div>
          </div>
        </div>
        
</template>


<script>
import Slide from '@/components/Slide.vue'

export default {
    name: 'Carousel',
    components: {
    Slide,
    },
    props: {

    },
    data(){
        return {
            slides:[
                {
                    id:1,
                    titre:'Collier',
                    image:'6.png',
                },
                {
                    id:2,
                    titre:'B.d\'orielle',
                    image:'2+.png',
                },
                {
                    id:3,
                    titre:'Bague',
                    image:'7.jpg',
                },
            ],
        }
    },
}
</script>
