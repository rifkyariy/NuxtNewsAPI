<template>
  <div class="p-10">  
    <!--Card 1-->
    <div class="max-w-sm rounded-lg overflow-hidden shadow-lg">
      <img class="w-full" :src="imgSrc" :alt="title">
      <div class="px-6 py-4">
        <div class="font-bold text-xl mb-2">{{ title }}</div>
        <p class="text-gray-700 text-base pb-4">
          {{ description }}
        </p>
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded" @click="redirectPage(url)">
          Detail
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: { 
    url: { type: String, default: '' },
    title: { type: String, default: '' }, 
    imgSrc: { type: String, default: '' },
    description: { type: String, default: '' },
  },
  methods: {
    redirectPage(url){
      window.location.href = url;
    }
  }
}
</script>

<style>

</style>