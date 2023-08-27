<script>
export default {
  name: "Jumbotron",
};
</script>

<template>
  <div
    class="h-60 bg-contain bg-no-repeat md:h-screen jumbotron lg:bg-cover lg:h-screen"
  >
    <!-- dekstop -->
    <div class="hidden lg:block md:block xl:block">
      <div
        class="w-1/2 h-96 flex flex-col justify-center items-center lg:h-screen lg:gap-6"
      >
        <div class="mx-8 lg:ms-20 text-white">
          <h1 class="text-4xl lg:text-6xl fontWitcher">The Witcher</h1>
          <p class="text-justify mt-2">
            Geralt of Rivia, a Solitary monter hunter, struggles to find his
            place in a world where people often prove more wicked than beast
          </p>
          <div class="flex gap-5 text-md mt-2">
            <p>2019</p>
            <div
              class="border-2 border-white px-3 rounded-md shadow-sm shadow-slate-600"
            >
              <p>Tv Series</p>
            </div>
          </div>
          <button
            class="px-10 py-1 mt-2 rounded-sm bg-red-600 hover:scale-125 duration-100 hover:shadow-xl hover:shadow-black"
          >
            Watch now!
          </button>
        </div>
      </div>
    </div>

    <!-- mobile -->
    <div class="block lg:hidden md:hidden xl:hidden">
      <div class="w-1/2 h-28 flex justify-center items-center">
        <div class="mt-16 text-white">
          <h1 class="text-2xl fontWitcher">The Witcher</h1>
          <div class="flex gap-2 text-md mt-2 text-xs items-center">
            <p>2019</p>
            <div
              class="border-2 border-white px-3 rounded-md shadow-sm shadow-slate-600"
            >
              <p>Tv Series</p>
            </div>
          </div>
          <button
            class="px-2.5 py-1 rounded-sm text-white mt-2 bg-red-600 text-sm"
          >
            Watch now!
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<style>
@import url("https://fonts.cdnfonts.com/css/superdie");

.jumbotron {
  background-image: url(https://s3-alpha-sig.figma.com/img/81a9/1f16/f4a45d07e18a63bbfeb7b17c1ee55dc0?Expires=1693785600&Signature=np~RjcRrMrZztKqLPkm75DqZXvAvfLJKDbp2Nh8q6AcD2fFDqUdE1uoaKHzRHKwnIn7rTCLyTph1Y~ZeZ9tnIhj9aqebpSaJOQ7Um7laKGs27xByJAMdhE7p1~qjqfKfRS6cqT8MYh-tCfdyK62Qr-O5c3hp94pSYPDxU03wQBR0JgNRcIQXWxedUGoywKJjvlNztipSHQ5iWdlsyivG3r2glnyMmaIbDG9~KPcZA8I4gQA42PtImBTiQT-kCTtHK39bGyGZY3~V~2phWMGSIm6tOCdOkyES3odjiHZn5QBBep9VNbDpbciYho5OZNMIwOeXlGOC-yeVgBmRf0wbgA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4);
}

.fontWitcher {
  font-family: "Superdie", sans-serif;
}
</style>
