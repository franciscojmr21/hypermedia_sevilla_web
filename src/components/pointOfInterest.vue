<template>


    <!-- single Point Of Interest -->

          <!-- first item -->
    <div class="col-sm-6">
            <div class="pointOfInterest-item">
              <marco>
              <img :src=imgPost() class="card-img-top car-img" alt="">
              <img_text class="centrado">{{this.title}}</img_text>
            </marco>
            </div>
          </div>
          <!--end of Point Of Interest -->
</template>


<script >

export default {
    props: {
        title: String, 
        photo: Image, 
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
   /* point of interest  */
.pointOfInterest-item{
  background: var(--mainYellow);
  position: relative;
  cursor: pointer;
}
.pointOfInterest-img{
  transition: all 1s ease-in-out;
}
.pointOfInterest-item:hover .pointOfInterest-img{
opacity: 0.5;
}

.pointOfInterest-item:hover .centrado{
  visibility: visible;
  }
.pointOfInterest-item::after{
  content: "";
  position: absolute;
 top: 0;
 left: 0;
 width: 100%;
 height: 100%;
 outline: 0.5rem solid var(--mainWhite);
 outline-offset: -2rem;
 transition: all 1s ease-in-out;
 transform: scale(0);
}
.pointOfInterest-item:hover:after{
  transform: scale(1);
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