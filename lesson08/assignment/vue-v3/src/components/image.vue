
<template>
 	<article class="post">
		<h3 class="post__title">{{ post.title }}</h3>
		<h6 class="post__img">{{ post.img}}</h6>
		<p class="post__alt">{{ post.alt }}</p>
	
    </article>
</template>

<script>
export default {
  name: 'post',
  props: ['post'],
  
}

</script>

