<template>
 <header>
      <!-- place navbar here -->
      <nav class="navbar ">
        <div class=" topnavbar container-fluid">
          <button
            class="navbar-toggler bmenu"
            type="button"
            data-bs-toggle="offcanvas"
            data-bs-target="#offcanvasNavbar"
            aria-controls="offcanvasNavbar"
          >
            <span class="navbar-toggler-icon"></span>
          </button>
          <div
            class="offcanvas offcanvas-start divmenu"
            tabindex="-1"
            id="offcanvasNavbar"
            aria-labelledby="offcanvasNavbarLabel"
          >
            <div class="offcanvas-header">
              <h5 class="offcanvas-title" id="offcanvasNavbarLabel">Menu</h5>
              <button
                type="button"
                class="btn-close"
                data-bs-dismiss="offcanvas"
                aria-label="Close"
              ></button>
            </div>
            <div class="offcanvas-body ">
              <ul class="navbar-nav justify-content-end flex-grow-1 pe-3">
                <li class="nav-item">
                  <a class="nav-link active" aria-current="page" href="#"
                    ><b>Acceuil</b></a
                  >
                </li>
                <li class="nav-item">
                  <a class="nav-link" href="#"><b>Cartes Cadeaux</b></a>
                </li>
                <li class="nav-item dropdown">
                  <a
                    class="nav-link dropdown-toggle"
                    href="#"
                    role="button"
                    data-bs-toggle="dropdown"
                    aria-expanded="false"
                  >
                    <b>Bijoux</b>
                  </a>
                  <ul class="dropdown-menu bBijoux">
                    <li><a class="dropdown-item" href="#">Collier</a></li>
                    <li>
                      <a class="dropdown-item" href="#">Bague</a>
                    </li>

                    <li>
                      <a class="dropdown-item" href="#">B.d'orielle</a>
                    </li>
                    <li>
                      <a class="dropdown-item" href="#">Bracelet</a>
                    </li>
                    <li>
                      <a class="dropdown-item" href="#">Montre</a>
                    </li>
                  </ul>
                </li>
              </ul>
              <br />
              <div class="conn">
                <ul>
                  <li>
                    <a class="connecte" href="#">Se connecte</a>
                  </li>
                  <li>
                    <a class="connecte" href="#">Créer un compte</a>
                  </li>
                  <li>
                    <a class="connecte" href="#">Contacter-nous</a>
                  </li>
                  <li>
                    <a class="connecte" href="#">Condition Générales</a>
                  </li>
                </ul>
              </div>
              <br />
              <br />

              <footera class="sc">
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
                <a href="#"><i class="fa-brands fa-youtube"></i></a>
               </footera>

              <!-- <form class="d-flex mt-3" role="search">
                <input
                  class="form-control me-2"
                  type="search"S
                  placeholder="Search"
                  aria-label="Search"
                />
                <button class="btn btn-outline-success" type="submit">
                  Search
                </button>
              </form> --> 
            </div>
          </div>
           <img src="../assets/logo2.png" alt="logo" width="250" height="200" /> 
          <div  >
          <span>
            <a class="bsearch" href="#"
              ><i class="fa-solid fa-magnifying-glass"></i
            > </a>
          </span>
           <span>
            <a class="bpanier" href="#"
              ><i class="fa-solid fa-bag-shopping"></i
            > 
              <!-- <span id="notification">{{ajout}}</span>  -->
              
             <!-- <span id="prixtotal">{{ totalPrix.toFixed(2) }} €</span>  -->
              
              </a>
          </span>
        </div>
        </div>
        <div class="   container  justify-content-center"  >
           <p class="item"><router-link class="nav-link" to="/">Home</router-link> </p> 
           <p class="item"><router-link class="nav-link" to="/Bijoux">Bijoux</router-link> </p>
           <p class="item"><router-link class="nav-link" to="/Cartes Cadeaux">Cartes Cadeaux</router-link> </p>
           
        </div>
         
        
         
        
      
      </nav>
    </header>

</template>

<script>
export default {
  name: 'Header',
  props: { 
    id: Number,
    titre:String,
    image:String,
  }
}
</script>


<style>
.divmenu {
  background-color: #e7d4cf;

  text-align: start;
  margin: 10px 0px 0px 20px;
  border-radius: 10px 10px 0px 0px;
  box-shadow: 0px 0px 40px gray;
}
</style>

