<template>
  <div class="gallery">
    <div class="card" v-for=" img in images" :key="img.id">
        <img :src="img.image" :alt="img.image">
    </div>
  </div>
</template>

<script>
export default {
      name: 'MyGallery',
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
                    image: require('../assets/Christian.png')
                },
                {
                    id: 'img4',
                    image: require('../assets/29.1.jpg')
                },
                {
                    id: 'img5',
                    image: require('../assets/18.jpg')
                },
                {
                    id: 'img6',
                    image: require('../assets/11.jpg')
                },
                {
                    id: 'img7',
                    image: require('../assets/10.jpg')
                },
                {
                    id: 'img8',
                    image: require('../assets/8.jpg')
                },
                {
                    id: 'img9',
                    image: require('../assets/7.1.jpg')
                },
                {
                    id: 'img10',
                    image: require('../assets/_DSF9666.jpg')
                },
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