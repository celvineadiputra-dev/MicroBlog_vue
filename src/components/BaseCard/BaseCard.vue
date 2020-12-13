<template>
  <div class="blog-post">
    <div class="blog-thumbnail">
      <a href="#" title="">
        <img src="https://via.placeholder.com/2172x1448" alt="" class="w-100">
      </a>
      <span class="category">English, Teachers, Shelly</span>
    </div>
    <div class="blog-info">
      <ul class="meta">
        <li><router-link to="/" title="">17/09/2020</router-link></li>
        <li><router-link to="/" title="">by Admin</router-link></li>
        <li><img src="assets/img/icon13.png" alt="" /><a href="#" title="">Teachers,</a><a href="#"
            title=""> School</a></li>
      </ul>
      <h3 class="stick"><router-link to="/" title="" class="a">Standard Post Sticky</router-link></h3>
      <p>Nullam erat dolor, hendrerit id turpis laoreet, congue dapibus odio. Duis tempor eros
        tortor, a ornare arcu egestas quis. Donec vehicula eget quam maximus interdum. Duis ultrices
        sapien eget metus luctus finibus. Morbi nec lobortis ante, sed condimentum nisl. Nam laoreet
        ullamcorper magna et fringilla</p>
      <router-link to="/" title="" class="read-more">Read <i
          class="fa fa-long-arrow-alt-right"></i></router-link>
    </div>
  </div>
</template>

<script>
  export default {
      name : "BaseCard"
  }

</script>

<style lang="scss" scoped>
a{
    text-decoration: none;
}
.stick{
    .a{
        color: #2b2b2b;
        &:hover{
            color: #1260a0;
        }
    }
}
</style>
