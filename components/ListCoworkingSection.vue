<template>
  <section class="my-[150px]">
    <div class="container">
      <div class="w-full">
        <h2 class="text-3xl font-bold">Ruang Kerja di dekatmu</h2>
      </div>

      <div class="my-14 grid gap-x-8 md:grid-cols-2 lg:grid-cols-3">
        <div
          v-for="(imageSrc, index) in listImageWorkingSpace"
          :key="index"
          class="w-full mb-20"
        >
          <div class="bg-white">
            <img :src="imageSrc.src" class="w-full rounded-xl" />

            <div class="mt-4">
              <h3>
                <a href="#" class="text-lg font-bold text-teal-500">
                  Lorem ipsum dolor sit amet.</a
                >
              </h3>
              <p class="my-1 text-base font-light text-gray-500">
                Lorem, ipsum dolor.
              </p>
              <h5 class="text-base font-normal"><b>Rp. 150000</b> / hari</h5>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      listImageWorkingSpace: [
        { src: 'images/1.jpg' },
        { src: 'images/2.jpg' },
        { src: 'images/3.jpg' },
        { src: 'images/4.jpg' },
        { src: 'images/5.jpg' },
        { src: 'images/6.jpg' },
      ],
    }
  },
}
</script>
