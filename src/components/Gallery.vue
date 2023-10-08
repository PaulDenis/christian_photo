<template>
  <div class="gallery">
    <div class="card" v-for=" img in images" :key="img.id">
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
                    id: 'img1',
                    image: require('../assets/foto_sfondo.jpg')
                },
                {
                    id: 'img2',
                    image: require('../assets/logo_temporaneo.jpg')
                },
                {
                    id: 'img3',
                    image: require('../assets/logo.png')
                }
            ]
         }
      }
   }
</script>

<style scoped lang="scss">

.gallery {
    display: flex;
    flex-wrap: wrap;
}
    .card {
        width: 40vw;
        height: auto;
        margin: 5%;
        padding: 2%;
        color: white;
        background-color: rgba(0, 0, 0, 0.7);
        img {
            width: 100%;
            height: auto;
        }
    }
</style>