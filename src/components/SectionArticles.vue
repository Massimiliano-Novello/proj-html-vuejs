<script>
export default {
  name: "SectionArticles",
  data() {
    return {
      cards: [
        {
          image: "photo-1444213007800-cff19e1677ac-600x450.jpg",
          title: "Undertanding community complexities",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Esse e Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit delectus voluptatum dolorem magni"
        },
        {
          image: "img-1-articles.jpg",
          title: "The uman story of uniqueness",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit delectus voluptatum dolorem magni",
        },
        {
          image: "img-2-articles.jpg",
          title: "Sustainable trade tactics",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit delectus voluptatum dolorem magni",
        },
        {
          image: "img-3-articles.jpg",
          title: "Farmes making a difference",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit delectus voluptatum dolorem magni",
        },
        {
          image: "img-4-articles.jpg",
          title: "Meeting remote tribes in Perù",
          text: "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Velit delectus voluptatum dolorem magni",
        },
      ],
      activeIndex: 0,
      intervall: null
    };
  },
  mounted () {
    this.autoplay()
  },
  methods: {
    getImagePath(imagePath) {
      return new URL(imagePath, import.meta.url).href;
    },
    clickedImg (clickIndex) {
      console.log("click");
      this.activeIndex = clickIndex
    },
    showNext () {
      if (this.activeIndex < this.cards.length - 1) {
        this.activeIndex++
      } else {
        this.activeIndex = 0
      }
    },
    autoplay () {
      this.intervall = setInterval(this.showNext, 2000)
    },
    stopAutoplay () {
      clearInterval(this.intervall)
    }
  },
};
</script>

<template>
  <section class="section-articles">
    <div class="title text-center">
      <h2>LATEST ARTICLES</h2>
      <div class="border-title my-3"></div>
      <p>Together we make all the difference</p>
    </div>
    <div class="aticles-content row">
      <div class="large-container col-lg-6 col-md-12 py-2">
        <div tabindex="0" @mouseover="stopAutoplay" @mouseout="autoplay">
          <img
          :src="getImagePath(`../assets/img/${cards[activeIndex].image}`)"
          alt=""
          />
          <div class="content-large-container">
            <h6 class="py-3">{{cards[activeIndex].title}}</h6>
            <p>
              {{ cards[activeIndex].text }}
            </p>
          </div>
        </div>
      </div>
      <div class="small-container col-lg-6 col-md-12 py-2">
        <div class="my_card d-flex" v-for="(item, index) in cards" :key="index" @click="clickedImg(index)">
          <img :src="getImagePath(`../assets/img/${item.image}`)" alt="" />
          <div class="content ms-2">
            <h6>{{ item.title }}</h6>
            <p>{{ item.text }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <div class="small-articles-section d-flex justify-content-center align-items-center">
      <h6 class="text-white">VIEW ALL OUR ARTICLES</h6>
  </div>
</template>

<style lang="scss" scoped>
.section-articles {
  width: 60%;
  margin: 0 auto;
  padding: 80px 0;


  .aticles-content {
    .large-container {
      height: 100%;
      margin-top: 10px;
      img {
        width: 100%;
      }
      .content-large-container {
        h6 {
          color: #fcd66c;
        }

        p {
          font-size: 0.8rem;
        }
      }
    }

    .small-container {
      .my_card {
        height: calc(100% / 4 - 20px);
        margin-top: 10px;
        cursor: pointer;
        img {
          width: 100px;
          object-fit: cover;
        }

        h6 {
            color: #fcd66c;
        }

        p {
            font-size: .7rem;
        }
      }
    }
  }
}
.small-articles-section {
  height: 80px;
  background-color: #ed6864;
}
</style>
