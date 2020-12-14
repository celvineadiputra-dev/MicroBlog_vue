<template>
  <div class="home">
    <BaseNavbar menu="Home"/>
    <BaseHero title="MickroBlog" subTitle="Selamat Datang Lengkapi Hari Mu dengan Coding"/>
    <section class="page-content text-left">
      <div class="container">
        <div class="row">
          <div class="col-lg-9">
            <div class="blog-section p-0 posts-page">
              <div class="blog-posts">
                <div v-if="isLoading">Loading....</div>
                <div v-if="isOffline" class="text-center">
                  <img src="/img/svg/Astronaut.svg" alt="Astronaut" class="img-fluid astro" width="300">
                  <h3>Anda Sedang Offline</h3>
                </div>
                <BaseCard
                  v-else
                  v-for="item in dataBlog"
                  :key="item.id"
                  :id="item.id"
                  :urlImage="item.urlImage"
                  :category="item.category"
                  :date="item.date"
                  :author="item.author"
                  :tag="item.tag"
                  :title="item.title"
                  :subContent="item.subContent"
                  :content="item.Content"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
// @ is an alias to /src
import BaseNavbar from '@/components/BaseNavbar/BaseNavbar.vue';
import BaseHero from "@/components/Hero/BaseHero";
import BaseCard from "@/components/BaseCard/BaseCard";
export default {
  name: "Home",
  data() {
    return {
      isLoading: true,
      isOffline: false,
      dataBlog: [],
    };
  },
  components: {
    BaseHero,
    BaseCard,
    BaseNavbar,
  },
  created() {
    this.getData();
  },
  methods: {
    //Fetch with header
    // headers:{
    //       "secret-key" : "$2b$10$c.prlR0rbYnG1km2GD0aSuqglF2aDwPF807vHI425GSmP1IWhMkBm"
    //     }
    getData() {
      fetch("https://api.npoint.io/c01566ca8f299f5fdf18")
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
          // console.log(data[0].Content);
          this.dataBlog = data;
          this.isLoading = false;
        }).catch(e=>{
          this.isOffline = true;
          this.isLoading = false;
        });
    },
  },
};
</script>


<style lang="scss" scoped>
.astro{
  animation-name: TopDown;
  animation-direction: alternate;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  animation-timing-function: ease-in-out;
}
@keyframes TopDown {
  from{
    transform: translateY(-20px);
  }
  to{
    transform: translateY(100px);
  }
}
</style>