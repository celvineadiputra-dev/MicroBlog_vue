<template>
  <div class="blog-post">
    <div class="blog-thumbnail">
      <a href="#" title="">
        <img v-bind:src="urlImage" alt="" class="w-100">
      </a>
      <span class="category">{{category}}</span>
    </div>
    <div class="blog-info">
      <ul class="meta">
        <li><router-link to="/" title="">{{date}}</router-link></li>
        <li><router-link to="/" title="">{{author}}</router-link></li>
        <li><img src="assets/img/icon13.png" alt="" /><a href="#" title="">{{tag}}</a></li>
      </ul>
      <h3 class="stick"><router-link to="/" title="" class="a">{{title}}</router-link></h3>
      <p>{{subContent}}</p>
      <router-link to="/" title="" class="read-more">Read <i
          class="fa fa-long-arrow-alt-right"></i></router-link>
    </div>
  </div>
</template>

<script>
  export default {
      name : "BaseCard",
      props: {
        id : Number,
        urlImage : String,
        category : String,
        date : String,
        author : String,
        tag: String,
        title : String,
        subContent : String, 
        content : String
      }
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
