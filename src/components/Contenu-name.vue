<template>

    <div class="container mt-5">
        <h1>Appel à une API</h1>
        <img v-bind:src="urlImg" alt="">
    </div>
    
</template>


<script>
import axios from 'axios'

export default {
    name: 'Contenu-name',
    data() {
        return {
            urlImg: null
        }
    },
    methods: {
        
    },
    mounted() {
        axios
        .get('https://api.thecatapi.com/v1/images/search')
        .then(reponse => {
            console.log(reponse);
            this.urlImg = reponse.data[0].url
        })
    }
}

</script>

<style>

h1 {
    margin-top: 100px!important;
}

.onglets {
    height: 250px;

}

</style>