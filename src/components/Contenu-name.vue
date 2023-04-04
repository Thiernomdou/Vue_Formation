<template>
    <div class="container mt-5">

        <h1>{{ titre }}</h1>

        <liste v-bind:myArr="myArr" :txt="txt" v-on:changeTitre="changementTitre($event)"></liste>

    </div>
    
</template>


<script>
import Liste from './Liste/Liste-fruits.vue'

export default {
    name: 'Contenu-name',
    data() {
        return {
            myArr: [
                {titre: 'Inception', date: 2010},
                {titre: 'Avatar', date: 2009},
                {titre: 'Seven', date: 1995}
            ],
            txt: 'Hello World',
            titre: 'Je suis le Titre'
        }
    },
    methods: {
        changementTitre: function(nvTitre) {
            this.titre = nvTitre;
        }
    },
    components: {
        'liste': Liste
    }
}

</script>

<style>

h1 {
    margin-top: 100px!important;
}

</style>