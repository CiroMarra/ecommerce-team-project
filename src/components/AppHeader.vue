<script>
import HeaderHero from './HeaderHero.vue'
export default {
  name: 'HeaderHero',
  
  components:{
    HeaderHero
  },
  props:{
    links: Array
  },
  mounted ()
  {
    console.log(this.links)
  },

  
  data() {
    return {
      shops: [
    {
        title: "Sony PS5 White",
        price: "Quality: $254",
        image: "./src/assets/img/cart1.png"
    },
    {
        title: "A4 Tec Mouse",
        price: "Quality: $121",
        image: "./src/assets/img/cart2.png"
    },
    {
        title: "Gear VR Led ",
        price: "Quality: $514",
        image: "./src/assets/img/cart3.png"
    },
]
      
  
    }
  }
}
  
</script>


<template>
   
  <header>
    <div class="bg-overlay">
      <nav class="navbar navbar-expand-lg bg-body-tertiary">
  <div class="container-fluid">
    <a class="navbar-brand" href="#">Navbar</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
        <li class="nav-item dropdown">
          <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
            Dropdown
          </a>
          <ul class="dropdown-menu">
            <li><a class="dropdown-item" href="#">Action</a></li>
            <li><a class="dropdown-item" href="#">Another action</a></li>
            <li><hr class="dropdown-divider"></li>
            <li><a class="dropdown-item" href="#">Something else here</a></li>
          </ul>
        </li>
        <li class="nav-item">
          <a class="nav-link disabled" aria-disabled="true">Disabled</a>
        </li>
      </ul>
      <form class="d-flex" role="search">
        <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
        <button class="btn btn-outline-success" type="submit">Search</button>
      </form>
    </div>
  </div>
</nav> 
                <div class="offcanvas offcanvas-end" tabindex="1" id="offcanvasRight" aria-labelledby="offcanvasRightLabel">
                  <div class="offcanvas-header">
                    <h5 class="offcanvas-title" id="offcanvasRightLabel">Offcanvas right</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="offcanvas" aria-label="Close"></button>
                  </div>
                  <div class="offcanvas-body">
                    <div class="">
                      <div class="item" v-for="item in shops" :key="item.id">            
                        <div class="card mb-3">
                           <div class="row g-0">
                              <div class="col-md-4">
                                <img :src="item.image" class="test">
                              </div>
                              <div class="col-md-8">
                                <div class="card-body gap-1">
                                  <h5 class="card-title">{{ item.title }}</h5>
                                  <p class="card-text">{{ item.price }} <svg class="svg-canvas svg-inline--fa fa-xmark" aria-hidden="true" focusable="false" data-prefix="fas" data-icon="xmark" role="img" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512" data-fa-i2svg=""><path fill="currentColor" d="M310.6 361.4c12.5 12.5 12.5 32.75 0 45.25C304.4 412.9 296.2 416 288 416s-16.38-3.125-22.62-9.375L160 301.3L54.63 406.6C48.38 412.9 40.19 416 32 416S15.63 412.9 9.375 406.6c-12.5-12.5-12.5-32.75 0-45.25l105.4-105.4L9.375 150.6c-12.5-12.5-12.5-32.75 0-45.25s32.75-12.5 45.25 0L160 210.8l105.4-105.4c12.5-12.5 32.75-12.5 45.25 0s12.5 32.75 0 45.25l-105.4 105.4L310.6 361.4z"></path></svg></p>
                                </div>
                              </div>
                            </div>
                        </div>
                      </div>
                    </div>
                      <div class="total-price d-flex justify-content-between align-items-center">
                        <div class="order text-white">Total Order</div>
                        <div class="cost text-white">$854.00</div>
                      </div>
                    <div class="bottone d-flex justify-content-center align-items-center py-5">
                      <button class="ms-btn">CHECK OUT</button>
                    </div>
                    
                  </div>
                </div>
    
    <AppHero></AppHero>
    
    </div>
     
    
  </header>


</template>





<style scoped>

.cost {
  padding-right: 10px;
}

.ms-btn {
  background-color: #05CC7C;
  font-weight: bolder;
  color: #191935;
  width: 250px;
  height: 50px;
}

.svg-canvas {
  width: 11px;
  color: #05CC7C;

}

.card {
  background-color: transparent;
  border: none;
  color: white;
}


.offcanvas, .offcanvas-header {
  background-color: transparent;

}


.offcanvas-body, .offcanvas-header {
  background-color: rgba(20, 20, 46, 0.5)
}

.test {
  border: #05CC7C solid 1px;
  width: 100px;
  height: 80px;
}

.ms-buttone {
  border: none;
  background-color: transparent;
}

.circle-box {
  width: 40px;
  height: 40px;
  background-color: white;
  display: flex;
  justify-content: center; 
  align-items: center; 
  border-radius: 50%;
  position: relative;
}
.svg {
  width: 20px;
  height: 20px;
  color: #333287;
}

.lcircle-box {
  width: 25px;
  height: 25px;
  background-color: #4350FF;
  display: flex;
  justify-content: center; 
  border-radius: 50%;
  position: absolute;
  bottom: 20px;
  left: 31px;
  color: white;
}

li {
  list-style: none;
}
a {
  text-decoration: none;
}
.ms-home-color {
  color: #05CC7C !important;
}

.navbar-nav .nav-link {
  color: white;
}

header {
  position: relative;
  background-image: url("../assets/img/banner1.png");
  height: 45vw;
  width: 100%;
  background-size:cover;
  background-repeat: no-repeat;
}

.bg-overlay{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 45vw;
  background-color: rgba(20, 20, 46, 0.5);
}

.drop-color {
  background-color: #202046;
}
.dropdown-item {
  color: #00AC4D;
}

.dropdown-menu:focus {
  color: white;
}
.navbar-nav .nav-link.show{
  color: white;
}
.navbar-nav {
  font-weight: bold;
}
</style>
