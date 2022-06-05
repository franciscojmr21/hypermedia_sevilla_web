<template>

    <!-- single Event -->
          <div class="col-10 mx-auto my-3 col-md-6 col-lg-4">
            <div class="card event-card">
              <a :href=url(general_url) target="_blank" rel="noopener noreferrer">
              <img :src=imgPost() class="card-img-top car-img" alt="">
              </a>
              <!-- card body -->
              <div class="card-body">
                <div class="event-info d-flex justify-content-between">
                  <!-- first flex child -->
                  <div class="event-text text-uppercase">
                    <h6 class="font-weight-bold">{{this.title}}</h6>
                    <h6>{{this.title2}}</h6> 
                  </div>
                  <!-- second flex child -->
                  <a :href=url(tickets_url) target="_blank" rel="noopener noreferrer">

                  <h5 class="event-value align-self-center py-2 px-3">
                    <span class="event-price">{{this.prize}}</span>
                  </h5>
                  
                </a>
                </div>
              </div>
              <!-- end of card -->
              <div class="card-footer text-capitalize d-flex justify-content-between" >
                <p><span></span>{{date}}</p>
                <a :href=url(location_url) target="_blank" rel="noopener noreferrer"><span></span>{{this.location_name}}<img src="../assets/maps.png"></a>
              </div>
            </div>
          </div>
          <!--end of single Event -->
</template>


<script >

export default {
    props: {
        title: String, 
        title2: String, 
        photo: Image, 
        general_url: URL, 
        tickets_url: URL, 
        prize: String, 
        date: String, 
        location_name: String, 
        location_url: URL
        },
        methods:{
            imgPost(){
                return this.photo;
            },
            url(url){
              return url;
            }
        }
}
</script>


<style >
@import url('https://fonts.googleapis.com/css?family=Roboto:400,700');

:root{
  --mainOrange:rgba(241, 99, 64, 0.7);
  --transparentOrange:rgba(241, 99, 64, 0.7);
  --mainWhite:#FFFFFF;
  --mainGrey:#9c9c9c;
  --mainBlack:#000000;
  --mainGrey:rgb(216, 214, 214);
  --mainYellow:#e3b505;
}
    /* Events */
.event{
  background: var(--mainGrey);
}
.event-card{
  border-radius: 0!important;
}
.event-img{
  border-top-left-radius: 0;
  border-top-right-radius: 0;
}
.event-value{
  background: var(--mainOrange);
  color: var(--mainWhite);
  clip-path: polygon(15% 0,85% 0,100% 100%,0 100%);
  transition: all 1s linear;
}
.event-value:hover{
  clip-path: polygon(0% 0,100% 0,100% 100%,0 100%);
}  

</style>