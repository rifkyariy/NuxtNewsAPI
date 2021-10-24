<template>
  <div class="grid grid-cols-4 gap-1">
    <NewsCard  v-for="list in news.articles" :key="list.id" :img-src="list.urlToImage" :title="list.title" :description="list.description" :url="list.url"/>
  </div>
</template>

<script>
export default {
  layout: 'header',
  async asyncData({ $axios }) {
    const news = await $axios.$get('https://newsapi.org/v2/everything?q=programming&domains=techcrunch.com,techinasia.com&apiKey=f217c7e5065f4a1281b5521039fc2e1f')
    return { news }
  },
}


</script>
