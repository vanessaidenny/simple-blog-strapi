<template>
  <BlogList :posts="data"></BlogList>
</template>

<script setup>
  const API_URL = 'https://my-blogposts-akl8.onrender.com/api/posts?populate[image][fields][0]=url&populate[authors][fields][0]=firstName&populate[authors][fields][1]=lastName&populate[authors][fields][2]=email'
  const { data } = await useFetch(API_URL)

</script>