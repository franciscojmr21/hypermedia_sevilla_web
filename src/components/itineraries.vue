<template>


    <!-- single Point Of Interest -->

          <!-- first item -->
 <!-- col -->
        <div class="col-8 mx-auto col-lg-6 col-md-4 my-3">
          <div class="itineary py-5 pl-4">
           <span class="itineary-icon">
              <i class="fas fa-cogs"></i>
            </span>
            <div class="img-container">
            <h6 class="text-capitalize itineary-title">{{title1}}</h6>
            <h5 class="text-uppercase font-weight-bold">{{title2}}</h5>
            </div>
          </div>
        </div>
        <!-- end col -->
</template>


<script >

export default {
    props: {
        title1: String, 
        title2: String, 
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
 /* itineary_form */
.itineary_form{
  background: var(--mainWhite);
}
.itineary_form-item{
  background: var(--mainWhite);
  border-radius: 0.5rem;
  opacity: 0.5;
  cursor: pointer;
  transition: all 1s ease-in-out;
}
.itineary_form-item:hover{
  opacity: 1;
  transform: scale(1.05);
}
.itineary_form-icon{
  font-size: 1.5rem;
  color: var(--mainYellow);
  cursor: pointer;
  transition: 0.5s all ease-in-out;
}
.itineary_form-icon:hover{
  color: var(--mainBlue);
}
.img-container{
  background: var(--mainBlue);
  position: relative;
  overflow: hidden;
}
.itineary_form-photo{
  transition: all 1s ease-in-out;
}
.img-container:hover .itineary_form-photo{
 transform: scale(1.3);
 opacity: 0.5;
}
.itineary_form-link{
  position: absolute;
  top: 50%;
  left: 50%;
  font-size: 3rem;
  transform: translate(-50%,-50%);
  color: var(--mainBlack);
  opacity: 0;
  transition:all 1s ease-in-out;
}
.itineary_form-link:hover{
  color: var(--mainWhite);
}

.img-container:hover .itineary_form-link{
  opacity: 1;
}


/*TEX OF POINT OF INTEREST*/

.centrado{
  color: white;
  text-shadow: black 0.2em 0.2em 0.5em;
  position: absolute;
  top: 50%;
  left: 50%;
  text-align: center;
  transform: translate(-50%, -50%);
}

img_text{
  visibility: hidden;
}

</style>