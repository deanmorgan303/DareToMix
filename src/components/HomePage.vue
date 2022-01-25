<template>
  <div
    :style="{
      'background-image': `url(https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/delish-horroscopecocktails-1617980845.png?crop=1.00xw:1.00xh;0,0&resize=980:*)`,
      width: '100%',
      height: '700px',
    }"
    class="image"
  >
    <div class="navContianer">
      <div><h3 class="navtext">Home</h3></div>
      <div><h3 class="navtext">Vote</h3></div>
      <div class="mainHead">
        <h3 class="navCenter">Beyond The Bar</h3>
        <h1>Dare To Mix</h1>
      </div>
      <div><h3 class="navtext">Watch Live</h3></div>
      <div><h3 class="navtext">SignUp</h3></div>
    </div>
  </div>

  <div class="infoBody">
    <div class="infocontainer">
      <h2 class="tittlewhite">FAN FAVORITE BARTENDER</h2>
      <p class="navtext">
        Click on the bartender image to vote for your FAVOURITE contestant. The
        contestant with the most votes will win the popular vote prize of JMD
        $100,000.
      </p>
    </div>

    <div class="infocontainer">
      <div class="mainHead">
        <h3 class="tittleRed">Mix & Watch</h3>
        <h3 class="tittlewhite">JANUARY 5TH starting @9:30 pm</h3>
      </div>
    </div>

    <div class="infocontainer">
      <div class="mainHead">
        <h3 class="tittlewhite">Round 4</h3>
        <h3 class="tittleRed">JDAVIOLL VS ROMAINE</h3>
      </div>
    </div>
  </div>

  <div class="bartenderbody">
    <div class="tittleBar">
      <img class="tittleIcon" :src="require('@/assets/bartender.png')" />
      <h4>The Bartenders</h4>
    </div>

    <div class="BartenderContianer">
      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender1.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender2.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender3.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender4.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender5.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender6.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender7.webp')"
        />
      </div>

      <div>
        <img
          class="bartenderImage"
          :src="require('@/assets/bartender8.webp')"
        />
      </div>
    </div>
  </div>

  <div>
    <div class="tittleBar">
      <img class="tittleIcon" :src="require('@/assets/bartender.png')" />
      <h4>Episodes</h4>
    </div>
    <div class="carouselstyle">
      <Carousel>
        <Slide v-for="(item, index) in someList" :key="index">
          <div class="carousel__item">
            <iframe
              width="1152"
              height="600"
              src="https://www.youtube.com/embed/Z4JPE9-Ec7U"
              title="YouTube video player"
              frameborder="0"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
              allowfullscreen
            >
            </iframe>
          </div>
        </Slide>

        <template #addons>
          <Navigation />
          <Pagination />
        </template>
      </Carousel>
    </div>
  </div>

  <div class="singup"> 
    <h1 class="navtext">Sign Up</h1>

  </div>
</template>

<script>
import { Carousel, Navigation, Pagination, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default {
  name: "Homepage",
  props: {
    msg: String,
  },
  data() {
    return {
      image: "./assets/backgroundCocktail.png",
      someList: [
        {
          html: "slide1",
          style: {
            background: "#1bbc9b",
          },
        },
        {
          html: "slide2",
          style: {
            background: "#4bbfc3",
          },
        },
        {
          html: "slide3",
          style: {
            background: "#7baabe",
          },
        },
        {
          html: "slide4",
          style: {
            background: "#7baabe",
          },
        },
      ],
    };
  },
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.mainHead {
  text-align: center;
}
.image {
  background-repeat: no-repeat;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
}
.navContianer {
  display: flex;
  justify-content: space-evenly;
  padding: 2%;
}

.navtext {
  color: #ffffff;
  font-family: "Lucida Handwriting";
}
.infoBody {
  display: flex;
  justify-content: space-evenly;
  margin-top: 2%;
  margin-bottom: 2%;
}
.infocontainer {
  background-color: #1a1a1a;
  width: 270px;
  height: 237px;
  border-radius: 3%;
  padding: 2%;
}
.tittlewhite {
  color: #ffffff;
  padding: 10px;
}
.tittleRed {
  color: #e93f33;
  padding: 10px;
}
.navCenter {
  color: #eeba5c;
}

.BartenderContianer {
  display: grid;
  grid-template-columns: auto auto auto auto;
  grid-gap: 10px;
  justify-content: space-between;
}
.bartenderbody {
  padding: 2%;
}
.tittleIcon {
  height: 60px;
  width: 60px;
}
.tittleBar {
  display: flex;
  padding: 10px;
}

.carousel__item {
  min-height: 600px;
  width: 80%;
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
.carouselstyle {
  justify-content: center;
  align-items: center;
  width: 80%;
} 
.singup{
  background-color: #1a1a1a;
  width:100%;
  height: 300px; 
  text-align: center;
}
</style>
