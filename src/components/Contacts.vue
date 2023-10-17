<template>
  <div class="contacts">
    <h3>Contattami</h3>
    <ul class="contact_list">
      <li>
        Mail: Photoentropy@esempio.com
      </li>
      <li>
        Telefono: <a href="tel:3202889772">+39 123 456 7890</a>
      </li>
      <li>
        Instagram: @Photoentropy
      </li>
    </ul>
  </div>
</template>

<script>
export default {
    name: 'ContactMe',
}
</script>

<style scoped lang="scss">

  .contacts {

    background-color: black;
    color: white;
    h3 {
      text-align: center;
      padding-top: 3vw;
    }
    .contact_list {
      margin-left: 3vw;
      list-style: none;

      li {
        margin-top: 2vw;
        &:last-child {
          padding-bottom: 5vw;
        }
      }
    }
  }
</style>