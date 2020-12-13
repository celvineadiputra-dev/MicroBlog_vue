<template>
  <header>
    <div class="container">
      <div class="header-content d-flex flex-wrap align-items-center">
					<div class="logo">
						<router-link to="/" title="">
							<img src="@/assets/logo.png" alt="h" srcset="@/assets/logo.png" width="50"> 
						</router-link>
					</div><!--logo end-->
					<div class="navigation-bar contact-add d-flex align-items-center justify-content-between">
					<nav>
						<ul>
							<li><router-link class="active" to="/" title="">Home</router-link></li>
							<li><router-link to="/" title="">About</router-link></li>
							<li><router-link to="/" title="">Contacts</router-link></li>
						</ul>
					</nav>
				</div>
					<div class="menu-btn">
						<router-link to="/">
							<span class="bar1"></span>
							<span class="bar2"></span>
							<span class="bar3"></span>
						</router-link>
					</div><!--menu-btn end-->
				</div><!--header-content end-->
      
    </div>
  </header>
  <MobileNavbar/>
</template>

<script>
import MobileNavbar from '../BaseNavbar/MobileNavbar'
export default {
  name: "BaseNavbar",
  components:{
    MobileNavbar
  }
};
</script>

<style lang="scss" scoped>
a{
  text-decoration: none !important;
}
</style>
