<template>
  <BaseNavbar menu="About" />
  <BaseHero title="About Me" subTitle="Celvine Adi Putra" />
  <section class="page-content text-left">
    <div class="container">
      <div class="row">
        <div class="col-lg-9">
          <h1 class="font-weight-bold biggerText">
            Welcome to <br />
            <label class="text-warning">MicroBlog</label>
          </h1>
          <div class="col-sm-12 col-md-6">
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Ipsam
              accusantium incidunt provident sint et pariatur, alias fugiat
              veritatis cupiditate ea neque nobis quibusdam odit facilis esse
              nihil doloremque quasi? Quis.
            </p>
            <i class="fab fa-instagram-square text-regular mr-2"></i>
            <i class="fab fa-facebook-square text-regular mr-2"></i>
            <i class="fab fa-github-square text-regular"></i>
          </div>
        </div>
      </div>
    </div>
    <div class="container mt-4">
      <div class="row">
        <div class="col-lg-6">
          place Image
        </div>
        <div class="col-lg-6">
          <h6 class="font-weight-bold text-warning">ABOUT ME</h6>
          <h1 class="font-weight-bold">Our Mission</h1>
          <div class="col-lg-9">
            <p>
              Praesent rhoncus justo erat, sed sollicitudin arcu malesuada vel.
              Etiam scelerisque justo ut purus luctus ullamcorper. Vivamus vitae
              elit ligula. Fusce eu rutrum nisl.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import BaseNavbar from "@/components/BaseNavbar/BaseNavbar.vue";
import BaseHero from "@/components/Hero/BaseHero";
export default {
  components: {
    BaseNavbar,
    BaseHero,
  },
};
</script>

<style scoped>
h1.biggerText {
  font-size: 48px;
  font-weight: bold;
}
.text-regular {
  font-size: 30px;
}
.fab {
  cursor: pointer;
}
.mr-2 {
  margin-right: 20px;
}
</style>