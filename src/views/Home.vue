<template>
  <div class="home">
    <BaseHero />
    <section class="page-content text-left">
      <div class="container">
        <div class="row">
          <div class="col-lg-9">
            <div class="blog-section p-0 posts-page">
              <div class="blog-posts">
                <div v-if="isLoading">Loading....</div>
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
import BaseHero from "@/components/Hero/BaseHero";
import BaseCard from "@/components/BaseCard/BaseCard";
export default {
  name: "Home",
  data() {
    return {
      isLoading: true,
      dataBlog: [],
    };
  },
  components: {
    BaseHero,
    BaseCard,
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
      fetch("https://api.jsonbin.io/b/5fd6c643bef8b7699e594206")
        .then((response) => response.json())
        .then((data) => {
          console.log(data);
          // console.log(data[0].Content);
          this.dataBlog = data;
          this.isLoading = false;
        });
    },
  },
};
</script>
