<template>
  <div class="home">
    <BaseHero />
    <section class="page-content text-left">
      <div class="container">
        <div class="row">
          <div class="col-lg-9">
            <div class="blog-section p-0 posts-page">
              <div class="blog-posts">
                <BaseCard />
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
    name: 'Home',
    components: {
      BaseHero,
      BaseCard
    },
  };

</script>
