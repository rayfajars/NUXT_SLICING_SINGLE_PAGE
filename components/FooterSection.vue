<template>
  <section>
    <div class="grid md:grid-cols-2">
      <div class="flex h-[800px] w-full bg-[#F6F6FB]">
        <div class="m-auto">
          <div class="px-[100px]">
            <div
              class="relative mb-12 h-16 w-16 items-center justify-center rounded-full bg-purple-700 p-5 text-center text-6xl shadow-xl"
            >
              <svg
                aria-hidden="true"
                class="w-4 h-4 text-white rotate-180 mx-auto"
                viewBox="0 0 24 27"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M14.017 18L14.017 10.609C14.017 4.905 17.748 1.039 23 0L23.995 2.151C21.563 3.068 20 5.789 20 8H24V18H14.017ZM0 18V10.609C0 4.905 3.748 1.038 9 0L9.996 2.151C7.563 3.068 6 5.789 6 8H9.983L9.983 18L0 18Z"
                  fill="currentColor"
                />
              </svg>
            </div>

            <h3 class="text-6xl font-bold">
              Apa kata <br />
              mereka tentang <br />
              ruang kerja
            </h3>
          </div>
        </div>
      </div>
      <div class="m-auto">
        <div class="px-[100px]">
          <div class="text-center">
            <h3 class="text-3xl font-semibold mb-7 px-24">
              Help us improve our productivity
            </h3>
            <p class="text-base font-normal px-20">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
              eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut
              enim ad minim veniam, quis nostrud exercitation ullamco laboris
              nisi ut aliquip ex ea commodo consequat.
            </p>
          </div>

          <hr class="w-[400px] mx-auto my-8 bg-gray-100 border-1 rounded" />

          <div class="swiper">
            <div class="swiper-wrapper">
              <div
                v-for="(imageSrc, index) in listImageWorkingSpace"
                :key="index"
                class="swiper-slide"
                :class="`slide--${index}`"
              >
                <div class="slider-content">
                  <div>
                    <img :src="imageSrc.src" class="rounded-full" />
                  </div>
                  <div class="text-center text-swiper mt-6">
                    <h4 class="font-bold text-sm">Lorem Saliba</h4>
                    <p class="font-light text-xs">Lorem, ipsum {{ index }}.</p>
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
// import Swiper JS
// add or remove unused modules
import { Swiper, Navigation, Pagination, Autoplay } from 'swiper'
import 'swiper/swiper-bundle.min.css'
export default {
  data() {
    return {
      listImageWorkingSpace: [
        { src: 'profile/1.jpg' },
        { src: 'profile/2.jpg' },
        { src: 'profile/3.jpg' },
        { src: 'profile/4.jpg' },
        { src: 'profile/5.jpg' },
        { src: 'profile/6.jpg' },
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
    const swiper = new Swiper('.swiper', {
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
      // slidesPerGroup: 1,
      centeredSlides: true,
      // Autoplay if needed
      autoplay: {
        delay: 5000,
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
.swiper {
  height: 300px;
  overflow: hidden;
  position: relative;
  width: 500px;
}
.swiper-slide {
  align-items: center;
  display: flex;
  justify-content: center;
}

.swiper-slide {
  /* filter: blur(1px); */
  @apply !blur-[2px];
}

.swiper-slide-active {
  @apply !blur-none;
}

.swiper-slide-active .slider-content img {
  @apply !h-24 !w-24;
}

.swiper-slide-next {
  @apply !blur-[1px];
}

.swiper-slide-next .slider-content img,
.swiper-slide-prev .slider-content img {
  @apply !h-20 !w-20;
}

.swiper-slide-next .slider-content .text-swiper,
.swiper-slide-prev .slider-content .text-swiper {
  @apply !invisible;
}

.swiper-slide-prev {
  @apply !blur-[1px];
}

.swiper-slide .slider-content img {
  /* filter: blur(1px); */
  @apply h-12 w-12;
}

.swiper-slide .slider-content .text-swiper {
  /* filter: blur(1px); */
  @apply invisible;
}

.swiper-slide-active .slider-content .text-swiper {
  @apply !visible;
}
</style>
