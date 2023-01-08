<template>
  <section class="my-[100px]">
    <div class="container">
      <div class="grid grid-cols-1 w-full">
        <div class="relative overflow-hidden rounded-lg cursor-pointer">
          <img
            src="container.jpg"
            class="rounded-lg h-[626px] w-[827px] float-right"
          />

          <div class="absolute top-0 left-0 px-6 py-32">
            <div class="mb-10">
              <h3 class="font-bold text-5xl">
                Temukan Ruang <br />
                Kerja Dimanapun
              </h3>
            </div>
            <div class="bg-white p-6 rounded-lg shadow-lg w-[460px]">
              <div class="grid grid-cols-2">
                <div>
                  <span class="text-gray-500 text-sm">
                    Temukan ruang kerja di</span
                  >
                  <select
                    class="border-0 cursor-pointer rounded-full w-40 text-xl font-bold mt-2"
                  >
                    <option>Jakarta</option>
                    <option>Bandung</option>
                    <option>Bali</option>
                  </select>
                </div>
                <div class="mx-auto">
                  <button
                    type="button"
                    class="text-white bg-[#FE753E] hover:bg-teal-500 focus:ring-4 focus:ring-teal-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 w-52 h-16"
                  >
                    Cari Sekarang
                  </button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
