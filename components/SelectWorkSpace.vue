<template>
  <section class="my-[100px]">
    <div class="container">
      <div class="grid grid-cols-2 px-20">
        <div>
          <h3 class="font-bold text-3xl">
            Pilih Ruang Kerja <br />
            Sesuai Keinginanmu
          </h3>
        </div>
        <div>
          <p class="text-gray-500 font-normal text-sm">
            Kami yakin kamu akan menemukan ruang kerja yang sesuai dengan
            keinginan dan seleramu. Kami memastikan kamu akan nyaman.
          </p>
          <a href="" class="font-bold text-sm text-teal-500"
            >Lihat semua jenis ruang kerja</a
          >
        </div>
      </div>
    </div>
    <div class="mt-20">
      <div class="swiper swiper-workspace">
        <div class="swiper-wrapper">
          <div
            v-for="(imageSrc, index) in listImageWorkingSpace"
            :key="index"
            class="swiper-slide"
            :class="`slide--${index}`"
          >
            <div class="slider-content mr-5">
              <div>
                <img :src="imageSrc.src" class="rounded-lg" />
              </div>
              <div class="relative w-[200px] -mt-24">
                <div class="bg-white p-6 rounded-lg shadow-lg">
                  <h4 class="mt-1 text-md font-bold uppercase text-teal-500">
                    A random Title
                  </h4>

                  <div class="mt-1">
                    <span class="text-gray-500 text-sm"> 12 Lokasi</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script scoped>
import { Swiper, Navigation, Pagination, Autoplay } from 'swiper'
import 'swiper/swiper-bundle.min.css'

export default {
  data() {
    return {
      listImageWorkingSpace: [
        { src: 'working-space/1.jpg' },
        { src: 'working-space/2.jpg' },
        { src: 'working-space/3.jpg' },
        { src: 'working-space/4.jpg' },
        { src: 'working-space/5.jpg' },
        { src: 'working-space/6.jpg' },
        { src: 'working-space/7.jpg' },
      ],
    }
  },
  mounted() {
    // configure Swiper to use modules. The modules were tested with SwiperJS v6.8.4 with NuxtJS v2.15.7
    // previously it was before export default. Moved here for performance issues. Move back in case of problems.
    // add or remove unused modules
    Swiper.use([Navigation, Pagination, Autoplay])

    // init Swiper:
    /* eslint-disable no-unused-vars */
    const swiper = new Swiper('.swiper-workspace', {
      // Optional parameters
      // @see https://swiperjs.com/swiper-api#parameters
      direction: 'horizontal',
      loop: true,
      // remove unused modules if needed
      modules: [Navigation, Pagination, Autoplay],
      // Pagination if needed
      pagination: {
        el: '.swiper-pagination',
        clickable: true,
      },
      loopFillGroupWithBlank: false,
      slidesPerView: 5,
      slidesPerGroup: 1,
      slidesOffsetAfter:100,
      slidesOffsetBefore:100,
      
      // Autoplay if needed
      autoplay: {
        delay: 3000,
      },
      // Navigation arrows if needed
      navigation: {
        nextEl: '',
        prevEl: '',
      },
      // Configure other options. Not tested
    })
  },
}
</script>


<style scoped>

.swiper-container {
  height: 300px;
  overflow: hidden;
  position: relative;
  width: 500px;
}
</style>