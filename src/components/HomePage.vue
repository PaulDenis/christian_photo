<template>
   <div class="banner">
      <img class="logo" src="../assets/logo_temporaneo.jpg" alt="logo">
      <h1>Photoentropy</h1>
      <!-- <ul class="orizontal_menu">
         <li @click="$emit('change_view', 'home')"
            :class="this.current_page == 'home' ? 'current' : ''">Home</li>
         <li @click="$emit('change_view', 'gallery')" 
            :class="this.current_page == 'gallery' ? 'current' : ''">My work</li>
         <li @click="$emit('change_view', 'about_me')"
            :class="this.current_page == 'about_me' ? 'current' : ''">About me</li>
         <li @click="$emit('change_view', 'contacts')"
            :class="this.current_page == 'contacts' ? 'current' : ''">Contacts</li>
      </ul> -->
   </div>
</template>
  
<script>
   export default {
      name: 'HomePage',
      props: {
         current_page: String
      },
      data() {
         return {
         }
      }
   }
</script>
  

<style scoped lang="scss">
  
   .banner {
      position: absolute;
      bottom: 25%;
      // height: 10%;
      width: 100%;
      text-align: center;
      background-color: rgba(0, 0, 0, 0.6);
      color: white;

      .logo {
         height: 100px;
         float: left;
         margin: 10px;
      }
      //This does not work on mobile
      // &:hover {
      //    cursor: pointer;
      //    background-color: rgba(0, 0, 0, 0.7);
      // }

      h1 {
         width: 30%;
         margin: auto;
         margin-top: 35px;
      }
   }
   .orizontal_menu {
      list-style: none;
      margin-top: 20px;
      margin-bottom: 20px;
      width: 90%;
      li {
         display: inline-block;
         margin-right: 15px;
      }
   }

   .current {
      border-bottom: 2px solid blue;
   }
</style>
  