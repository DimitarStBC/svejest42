<template>
  <div>
    <div class="homeSection d-flex align-items-start justify-content-between">
      <div class="d-flex flex-column align-items-start">
        <h1 class="itemMargin">Свежест 42</h1>
        <h2
          class="itemMargin"
        >Lorem ipsum dolor sit amet consectetur adipisicing elit. Eos, mollitia!</h2>
        <a class="btn btn-primary" href role="button">lorem</a>
      </div>
      <div>
        <img src="@/assets/waterLeaf.png" width="800" class="img-fluid anim" alt />
      </div>
    </div>

    <!--     
    <div class="marCorousel">
      <b-carousel class="d-flex align-items-center" :interval="3000">
        
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group class="d-flex justify-content-around align-items-center imgWidth">
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo1" overlay />
              </div>
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo2" overlay />
              </div>
            </b-card-group>
          </template>
        </b-carousel-slide>
       
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group class="d-flex justify-content-around align-items-center imgWidth">
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo3" overlay />
              </div>
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo4" overlay />
              </div>
            </b-card-group>
          </template>
        </b-carousel-slide>
        
        <b-carousel-slide>
          <template v-slot:img>
            <b-card-group class="d-flex justify-content-around align-items-center imgWidth">
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo5" overlay />
              </div>
              <div class="d-flex justify-content-around align-items-center">
                <img v-bind:src="logos.logo6" overlay />
              </div>
            </b-card-group>
          </template>
        </b-carousel-slide>
      </b-carousel>
    </div>-->

    <!-- about -->
    <div id="about">
      <About />
    </div>
    <div id="pricing">
      <Pricing />
    </div>
    <div id="contact">
      <Contact />
    </div>
  </div>
</template>

<script>
import About from "@/components/About";
import Pricing from "@/components/Pricing";
import Contact from "@/components/Contact";

export default {
  name: "Home",
  components: {
    About,
    Pricing,
    Contact,
  },
  data() {
    return {
      logos: {
        logo1: require("@/assets/logos/budmax.jpg"),
        logo2: require("@/assets/logos/danlex.png"),
        logo3: require("@/assets/logos/koush.png"),
        logo4: require("@/assets/logos/logos-ea.png"),
        logo5: require("@/assets/logos/MusalaSoft.jpg"),
        logo6: require("@/assets/logos/Park.png"),
      },
    };
  },
};
</script>

<style scoped>
.homeSection {
  height: 80vh;
}
.imgWidth {
  width: 100%;
}
.imgWidth img {
  height: 70px;
}
.homeSection {
  padding-top: 40px;
}
.marCorousel {
  height: 150px;
}
.anim {
  animation: sliding;
  animation-duration: 4s;
  animation-iteration-count: infinite;
  transform-origin: bottom left;
}
.itemMargin {
  margin: 20px 0;
}
@keyframes sliding {
  0% {
    transform: rotate(0deg);
  }
  50% {
    transform: rotate(1deg);
  }
  100% {
    transform: rotate(0deg);
  }
}
</style>