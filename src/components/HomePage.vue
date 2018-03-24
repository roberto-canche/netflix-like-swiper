<template>
  <swiper :options="swiperOption">
      <!-- Slides -->
      <swiper-slide>
        <Movies image="http://res.cloudinary.com/og-tech/image/upload/s--4NgMf3RF--/v1521804358/avengers.jpg" title="Avengers : Infinity War" description="Thanos is around" duration="2hrs"/>
      </swiper-slide>

      <swiper-slide>
        <Movies image="http://res.cloudinary.com/og-tech/image/upload/s--BmgguRnX--/v1521804402/thor.jpg" title="Thor : Ragnarok" description="Thor lost his hair" duration="2hrs30mins"/>
      </swiper-slide>

      <swiper-slide>
        <Movies image="http://res.cloudinary.com/og-tech/image/upload/s--qXaW5V3E--/v1521804426/wakanda.jpg" title="Black Panther" description="Wakanda Forever" duration="2hrs15mins"/>
      </swiper-slide>
        <!-- Control: opcional -->
      <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<style scoped>
.swiper-slide {
    display: flex;
    justify-content: center;
    flex-direction: column;
}
.swiper-container {
    height:500px;
}
</style>


<script>
import Movies from './Movies'
import 'swiper/dist/css/swiper.css'
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  name: 'HomePage',
  components: {
      Movies,
      swiper,
      swiperSlide
  },
  data() {
      return {
          swiperOption: {
              /*direction: 'vertical',
              pagination: {
                  el: '.swiper-pagination',
                  type: 'bullets'
              },*/
              effect: 'coverflow',
              grabCursor: true,
              centeredSlides: true,
              slidesPerView: '5',
              coverflowEffect: {
                  rotate: 50,
                  stretch: 0,
                  depth: 100,
                  modifier: 1,
                  slideShadows: false,
              },
              pagination: {
                  el: '.swiper-pagination'
              }
          }
      }
  }
}
</script>
