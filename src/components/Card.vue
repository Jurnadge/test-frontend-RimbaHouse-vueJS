<script>
export default {
  name: "Card",
  props: {
    img: String,
    title: String,
    year: Number,
  },
};
</script>

<template>
  <div
    class="text-white w-28 lg:w-56 md:w-44 xl:w-44 scale-75 hover:scale-90 duration-300"
  >
    <img class="object-cover rounded-t-md h-48 lg:h-96" :src="img" alt="" />
    <p>{{ title }}</p>
    <p>{{ year }}</p>
  </div>
</template>
