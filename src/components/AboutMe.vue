<template>
  <div>
    <img src="../assets/Christian.png" alt="Huskye">
    <h3>Chi sono</h3>
    <br>
    <p>Adoro tenere la Macchina Fotografica tra le mani e osservare la reazione delle persone per i miei lavori.<br>
        Musicista, fotografo e videomaker, ex Geometra.<br>
        Mi Diverto nel mentre che trasformo una passione in un lavoro.</p>
  </div>
</template>

<script>
export default {
    name: 'AboutMe',
    props: {

    }
}
</script>

<style scoped lang="scss">
div {
    padding: 5%;
    background-color: rgba(0, 0, 0, 0.7);

}
    img {
        width: 40vw;
        float: left;
        margin-right: 3%;
    }
    h3 {
        color: wheat;
        font-size: 30px;
    }
    p {
        color: white;
        font-size: 20px;
    }
</style>