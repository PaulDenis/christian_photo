<template>
   <div class="banner">
      <h1>Photoentropy</h1>
      <ul class="orizontal_menu">
         <li :class="pagina_corrente == 'home' ? 'current' : ''">Home</li>
         <li>My work</li>
         <li>About me</li>
         <li>Contacts</li>
      </ul>
   </div>
</template>
  
<script>
   export default {
      name: 'HomePage',
      props: {

      },
      data() {
         return {
            pagina_corrente: "home"
         }
      }
   }
</script>
  

<style scoped lang="scss">
  
   .banner {
      position: absolute;
      bottom: 15%;
      // height: 10%;
      width: 100%;
      text-align: center;
      background-color: rgba(0, 0, 0, 0.6);
      color: white;

      // &:hover {
      //    cursor: pointer;
      //    background-color: rgba(0, 0, 0, 0.7);
      // }

      //This does not work on mobile
      h1 {
         margin-top: 10px;
      }
   }
   .orizontal_menu {
      list-style: none;
      margin-top: 20px;
      margin-bottom: 20px;
      li {
         display: inline-block;
         margin-right: 15px;
      }
   }

   .current {
      border-bottom: 2px solid blue;
   }
</style>
  