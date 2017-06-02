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
                fotos: []
            }
        },
        created() {
            this.$http.get('http://localhost:3000/v1/fotos')
                .then(resp => resp.json());
                .then(fotos => this.fotos = fotos, err => console.log(err));
        }
    }
</script>

<style>

</style>
