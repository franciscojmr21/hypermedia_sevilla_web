<template>
  
  <body>
    <Navbar :item1="item1" :item2="item2" :item3="item3" :item4="item4" :item5="item5" :item6="item6" :logo="logo" :social1="social1" 
    :social2="social2" :social3="social3"></Navbar>
    <section class="event py-5" id="events">
      <div class="container">
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
  </body>
</template>

<script>
import Evento from './components/evento.vue'
import Navbar from './components/navbar.vue'

import e1_photo_ from './assets/Puro Latino.jpeg'
import e2_photo_ from './assets/cartel-semana-santa-sevilla-2022.jpg'
import e3_photo_ from './assets/feria_sevilla.jpg'
import logo from './assets/logo.png'

  
export default {
    name: 'App',
    components: {
    Evento,
    Navbar
},
    data: function() {
      return {
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
        social3: "https://www.instagram.com/ayto_sevilla/"
      };
    },
  };

</script>

<style>

div#evento1{
width: 348px;
height: 386px;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
