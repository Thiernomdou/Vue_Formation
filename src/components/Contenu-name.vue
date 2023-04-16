<template>
    <div class="container mt-5">

        <h1>{{ titre }}</h1>

        <div class="btn btn-outline-primary mr-2 mb-5" @click="toggleOnglet1">Onglet 1</div>
        <div class="btn btn-outline-primary mb-5" @click="toggleOnglet2">Onglet 2</div>

        <div class="card onglets mb-5">
            <texte-1 class="p-5" v-if="toggle1"></texte-1>
            <texte-2 class="p-5" v-if="toggle2"></texte-2>
        </div>


        <modale-text v-bind:revele="revele" v-bind:toggleModale="toggleModale"></modale-text>
        <div @click="toggleModale" class="btn btn-success">Ouvre la modale</div>


    </div>
    
</template>


<script>

import Texte1 from './Texte-1.vue'
import Texte2 from './Texte-2.vue'
import Modale from './Modal-text.vue'

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
            titre: 'Je suis le Titre',
            toggle1: true,
            toggle2: false,
            revele: false
        }
    },
    methods: {
        changementTitre: function(nvTitre) {
            this.titre = nvTitre;
        },
        toggleOnglet1: function() {
            this.toggle1 = true;
            this.toggle2 = false
        },
        toggleOnglet2: function() {
            this.toggle1 = false;
            this.toggle2 = true;
        },
        toggleModale: function() {
            this.revele = !this.revele;
        }
    },
    components: {
        'texte-1': Texte1,
        'texte-2': Texte2,
        'modale-text': Modale
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