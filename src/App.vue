<template>
  <div>
    <h1 v-text="titulo"></h1>

    <ul>
      <li v-for="foto of fotos">
        <img v-bind:src="foto.url" v-bind:alt="foto.titulo">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  data() {
    return {
      titulo: 'Alurapic',
      fotos: [
        {
          url: 'http://www.maedecachorro.com.br/wp-content/uploads/2017/01/cachorro-foto-de-divulga%C3%A7%C3%A3o.jpg',
          titulo: 'Dog'
        },
        {
          url: 'http://www.maedecachorro.com.br/wp-content/uploads/2017/01/cachorro-foto-de-divulga%C3%A7%C3%A3o.jpg',
          titulo: 'Dogao'
        }
      ]
    }
  }
}
</script>

<style>

</style>
