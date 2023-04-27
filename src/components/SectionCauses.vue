<script>
export default {
  name: "SectionCauses",
  data() {
    return {
      image: [
      "avada-charity-fair-trade-featured-200x150.jpg",
      "avada-charity-shelter-featured-200x150.jpg",
      "avada-charity-farming-featured-200x150.jpg",
      "avada-charity-vaccines-featured-200x150.jpg"
    ]
    };
  },
  methods: {
    getImagePath (image) {
      return new URL (image, import.meta.url).href
    }
  }
};
</script>

<template>
  <section class="section-causes">
    <div class="container">
      <div class="causes-title text-center">
        <h2>RECENT CAUSES</h2>
        <div class="border-title my-4"></div>
        <p>We run projects in over 30 countries in 5 continents</p>
      </div>
      <div class="image row">
        <img
          class="col-lg-3 col-md-6 mt-3" v-for="(item, index) in image" :key="index"
          :src="getImagePath(`../assets/img/${item}`)"
          alt=""
        />
      </div>
    </div>
</section>
<div class="small-causes-section d-flex justify-content-center align-items-center">
    <h4 class="text-white">View all or causes</h4>
</div>
</template>

<style lang="scss" scoped>
.section-causes {
    margin: 80px 0;

}
.small-causes-section {
    height: 100px;
    background-color: #ed6864;
}

</style>
