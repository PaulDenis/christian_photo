<template>
  <div>
    <div v-for=" img in images" :key="img">
        <img :src="img.image" :alt="img.image">
    </div>
  </div>
</template>

<script>
export default {
      name: 'HomePage',
      props: {

      },
      data() {
         return {
            images: [
                {
                    name: 'img1',
                    image: './assets/foto_sfondo.jpg'
                },
                {
                    name: 'img2',
                    image: '../assets/logo_temporaneo.jpg'
                },
                {
                    name: 'img3',
                    image: '../assets/logo.png'
                }
            ]
         }
      }
   }
</script>

<style>
    div {
        color: white;
    }
</style>