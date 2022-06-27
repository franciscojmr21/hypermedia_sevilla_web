<template>
  <html lang="en" class="fontawesome-i2svg-active fontawesome-i2svg-complete">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
  </head>
  <body>
    <main_header :title="main_title" :title2="main_title2"></main_header>
    <Navbar id="navbar_top" :item1="item1" :item2="item2" :item3="item3" :item4="item4" :item5="item5" :item6="item6" :logo="logo" :social1="social1" 
      :social2="social2" :social3="social3"></Navbar>
    <section class="event py-5" id="events">
      <div class="container">
         <!-- section title -->
        <div class="row mb-5">
          <div class="col d-flex flex-wrap text-uppercase justify-content-center">
            <!-- <h1 class="font-weight-bold align-self-center mx-1">most important</h1> -->
            <!-- <a href="Events.html#setas"> -->
            <h1 class="section-title--special mx-1">events</h1>
          <!-- </a> -->
          </div>
        </div>
        <div class="row">
          <Evento :title="e1_title" :title2="e1_title2" :photo="e1_photo" :general_url="e1_general_url" :tickets_url="e1_tickets_url"
          :prize="e1_prize" :date="e1_date" :location_name="e1_location_name" :location_url="e1_location_url" ></Evento>

          <Evento :title="e2_title" :title2="e2_title2" :photo="e2_photo" :general_url="e2_general_url" :tickets_url="e2_tickets_url"
          :prize="e2_prize" :date="e2_date" :location_name="e2_location_name" :location_url="e2_location_url" ></Evento>

          <Evento :title="e3_title" :title2="e3_title2" :photo="e3_photo" :general_url="e3_general_url" :tickets_url="e3_tickets_url"
          :prize="e3_prize" :date="e3_date" :location_name="e3_location_name" :location_url="e3_location_url" ></Evento>
        </div>
      </div>
    </section>

     

     <section class="pointsOfInterest py-5" id="points_of_interest">
       <div class="container">
         <!-- section title -->
        <div class="row mb-5">
          <div class="col d-flex flex-wrap text-uppercase justify-content-center">
            <!-- <h1 class="font-weight-bold align-self-center mx-1">most important</h1> -->
            <!-- <a href="Events.html#setas"> -->
            <h1 class="section-title--special mx-1">points of interest</h1>
          <!-- </a> -->
          </div>
        </div>
  <div class="row">
    <PointOfInterest :title="pI_title" :photo="pI_image" ></PointOfInterest>
    <div class="col-sm-6 d-flex flex-column justify-content-between">
       <div class="row">
         <PointOfInterest :title="pI_title" :photo="pI_image" ></PointOfInterest>
          <PointOfInterest :title="pI_title" :photo="pI_image" ></PointOfInterest>
       </div>
     
       <div class="row">
         <PointOfInterest :title="pI_title" :photo="pI_image" ></PointOfInterest>
          <PointOfInterest :title="pI_title" :photo="pI_image" ></PointOfInterest>
       </div>
       
 
    </div>
    


     
    </div>
    </div>

                       

    </section>


<!-- falta la foto -->
     
    <section class="services py-5" id="service_types">
    <div class="container">
       <!-- section title -->
        <div class="row mb-5">
          <div class="col d-flex flex-wrap text-uppercase justify-content-center">
            <!-- <h1 class="font-weight-bold align-self-center mx-1">most important</h1> -->
            <!-- <a href="Events.html#setas"> -->
            <h1 class="section-title--special mx-1">services</h1>
          <!-- </a> -->
          </div>
        </div>
       <div class="row">
         <div class="col-10 mx-auto col-lg-6 services-info my-3">
        <Service :title1="ser_title1" :title2="ser_title2"></Service>  <!-- no se pone en negrita -->
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>
        <Service :title1="ser_title1" :title2="ser_title2"></Service>

</div>
       <!-- services img -->
        <div class="col-10 mx-auto col-lg-6 services-img align-self-center my-3">
          <!-- img container -->
          <a href="Service.html">
          <div class="img-container">
             <img :src=imgPostServices() alt="" class="img-fluid services-photo">
            <a href="Service.html" class="services-link">
              <i class="fas fa-search"></i>
            </a>
          </div>
        </a>
        </div>
 
       </div>
      </div>


    </section>


<!-- poner video de fondo -->

  <section class="itinearies py-2 d-flex align-items-center" id="itinearies">
    <!-- video container -->
 <!-- <div class="video-container">
      <video class="video-item" autoplay loop muted>
        <source src="assets/videoBcg.mp4" type="video/mp4">Your browser does not support video tag
      </video>
    </div> -->
    <!-- end of video container -->
    <!-- video overlay -->
    <div class="video-overlay"></div>
    <!-- end of video overlay -->
    <!-- itineary content -->
    <div class="container py-5">
       <!-- section title -->
        <div class="row mb-5">
          <div class="col d-flex flex-wrap text-uppercase justify-content-center">
            <!-- <h1 class="font-weight-bold align-self-center mx-1">most important</h1> -->
            <!-- <a href="Events.html#setas"> -->
            <h1 class="section-title--special mx-1">itineraries</h1>
          <!-- </a> -->
          </div>
        </div>
      <div class="row my-3">
        <!-- col -->
         <Itinerary :title1="it_title1" :title2="it_title2"></Itinerary>
        <!-- end col -->
        <!-- col -->
        <Itinerary :title1="it_title1" :title2="it_title2"></Itinerary>
        <!-- end col -->
        <!-- col -->
        <Itinerary :title1="it_title1" :title2="it_title2"></Itinerary>
        <!-- end col -->
        <!-- end col -->
        <!-- col -->
        <Itinerary :title1="it_title1" :title2="it_title2"></Itinerary>
        <!-- end col -->
      </div>
    </div>
  </section>






  </body>
  
  </html>
</template>

<script>
import Evento from './components/evento.vue'
import PointOfInterest from './components/pointOfInterest.vue'
import Service from './components/services.vue'
import Itinerary from './components/itineraries.vue'
import Navbar from './components/navbar.vue'
import main_header from './components/main_header.vue'

import e1_photo_ from './assets/Puro Latino.jpeg'
import e2_photo_ from './assets/cartel-semana-santa-sevilla-2022.jpg'
import e3_photo_ from './assets/feria_sevilla.jpg'
import ser_photo_ from './assets/torre del oro.jpeg'
import logo from './assets/logo.png'

  
export default {


        methods:{
            imgPostServices(){
                return this.photoServices;
            },
            url(url){
              return url;
            }
        },

    name: 'App',
    components: {
    Evento,
    Navbar,
    PointOfInterest,
    Service,
    Itinerary,
    main_header
},

 props: {
        photoServices: Image,  
        },

    data: function() {
      return {

        main_title: 'Sevilla',
        main_title2: 'Has a Special Color',

        e1_title: 'Puro Latino',
        e1_title2: 'Festival',
        e1_photo: e1_photo_,
        e1_general_url: 'https://purolatino.es/sevilla/',
        e1_tickets_url: 'https://purolatino.es/sevilla/entradas/',
        e1_prize: '79 €',
        e1_date: '01/07/22 - 02/07/22',
        e1_location_name: 'Estadio Olímpico de La Cartuja',
        e1_location_url: 'https://goo.gl/maps/RNz2n9qG89YMjcMr5',

        e2_title: 'Semana Santa',
        e2_title2: '2022',
        e2_photo: e2_photo_,
        e2_general_url: "https://www.sevilla.org/fiestas-de-la-ciudad/semana-santa/",
        e2_prize: 'Free',
        e2_date: '10/04/22 - 16/04/22',
        e2_location_name: 'Sevilla Centre',
        e2_location_url: 'https://goo.gl/maps/htgB2xMuTrbaVJqc8',

        e3_title: 'Feria de Sevilla',
        e3_title2: '2022',
        e3_photo: e3_photo_,
        e3_general_url: 'https://www.sevilla.org/fiestas-de-la-ciudad/feria-de-sevilla',
        e3_prize: 'Free',
        e3_date: '01/05/22 - 07/05/22',
        e3_location_name: 'Between Los Remedios and Tablada',
        e3_location_url: 'https://goo.gl/maps/HyeFmoidtzKBtyEV8',

        item1: "ABOUT US", 
        item2: "POINTS OF INTEREST", 
        item3: "EVENTS", 
        item4: "ITINERARIES", 
        item5: "SERVICE TYPES", 
        item6: "CONTACT US", 
        logo: logo, 
        social1: "https://es-la.facebook.com/AyuntamientodeSevilla", 
        social2: "https://twitter.com/sevillaciudad", 
        social3: "https://www.instagram.com/ayto_sevilla/",

        pI_title: "Plaza de España",
        pI_image: "https://upload.wikimedia.org/wikipedia/commons/b/b6/Plaza_de_España_%28Sevilla%29_-_01.jpg",

        ser_title1: "Seville",
        ser_title2: "Tour Guide",

        it_title1: "Day",
        it_title2: "1",


        photoServices: ser_photo_


      };
    },
    created: function(){
      document.addEventListener("DOMContentLoaded", function(){
        window.addEventListener('scroll', function() {
          if (window.scrollY > document.getElementById('navbar_top').offsetTop){
            document.getElementById('navbar_top').classList.add('fixed-top');
            document.getElementById('navbar_top').classList.add('navbar-background');
          } else {
            document.getElementById('navbar_top').classList.remove('navbar-background');
            document.getElementById('navbar_top').classList.remove('fixed-top');
          } 
        });
      });
    }
  };












</script>

<style>




.section-title--special{
  background: var(--transparentOrange);
  color: var(--mainWhite);
  padding: 0.5rem 2rem;
  clip-path: polygon(10% 0, 100% 0, 90% 100%,0 100%);
}

/* Services */
.services{
  background: var(--mainGrey);
}
.services-item{
  background: var(--mainWhite);
  border-radius: 0.5rem;
  opacity: 0.5;
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}
.services-item:hover{
  opacity: 1;
  transform: scale(1.05);
}
.services-icon{
  font-size: 1.5rem;
  color: var(--mainYellow);
  cursor: pointer;
  transition: 0.5s all ease-in-out;
}
.services-icon:hover{
  color: var(--mainBlue);
}
.img-container{
  background: var(--mainBlue);
  position: relative;
  overflow: hidden;
}
.services-photo{
  transition: all 1s ease-in-out;
}
.img-container:hover .services-photo{
 transform: scale(1.3);
 opacity: 0.5;
}
.services-link{
  position: absolute;
  top: 50%;
  left: 50%;
  font-size: 3rem;
  transform: translate(-50%,-50%);
  color: var(--mainBlack);
  opacity: 0;
  transition:all 1s ease-in-out;
}
.services-link:hover{
  color: var(--mainWhite);
}

.img-container:hover .services-link{
  opacity: 1;
}



  /* Itineary section */

.itinearies{
  position: relative;
  min-height: 85vh;
  max-width: 95vw;
  margin: 0 auto;
  clip-path: polygon(0 10%,100% 0,100% 90%, 0 100%);
  
}
.video- {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: -3;
}
.video-item{
  width: 100%;
  height: 100%;
  object-fit: cover;
}
/* .video-overlay{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(rgba(241, 99, 64, 0.7), rgba(241, 99, 64, 0.7)), url(../img/la\ giralda\ fondo.jpg)center/cover fixed no-repeat;
  z-index: -2;
} */
.itineary{
  background: var(--mainBlack);
  color: var(--mainWhite);
  transition: all 0.5s ease-in-out;
}
.itineary:hover{
  background: var(--mainWhite);
  color: var(--mainBlack);
  padding-left: 2.2rem!important
}
.itineary-icon{
  font-size: 4rem;
  color: var(--mainYellow);
}

div#evento1{
width: 348px;
height: 386px;
}

/* div#pointOfInterest1{
width: 348px;
height: 386px;
} */

.col2 {
    border:2px solid green;
    width:49%;
    float:left;
    height:100%;
    margin-right:2%;    
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.navbar-background {
  padding: 5px 5px;
}
</style>
