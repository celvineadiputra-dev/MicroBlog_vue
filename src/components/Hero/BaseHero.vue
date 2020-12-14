<template>
  <section class="pager-section">
			<div class="container">
				<div class="pager-content text-center">
					<h2>{{title}}</h2>
					<h3>{{subTitle}}</h3>
				</div>
				<h2 class="page-titlee">{{title}}</h2>
			</div>
		</section>
</template>

<script>
export default {
	name : "BaseHero",
	props:{
		"title" : String,
		"subTitle" : String,
	}
}
</script>

<style>

</style>