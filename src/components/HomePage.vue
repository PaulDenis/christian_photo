<template>
   <div class="banner">
      <h1>Photoentropy</h1>
   </div>
</template>
  
<script>
   export default {
      name: 'HomePage',
      props: {

      },
   }
</script>
  

<style scoped lang="scss">
  
   .banner {
      position: absolute;
      bottom: 10%;
      height: 10%;
      width: 100%;
      text-align: center;
      background-color: rgba(0, 0, 0, 0.4);
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
</style>
  