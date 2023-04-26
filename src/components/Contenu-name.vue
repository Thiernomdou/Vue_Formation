<template>

    <div class="container mt-5">
        <h1>Notre premier Formulaire</h1>
       
       
        <form>


            <!-- input & textarea-->
            <div class="form-group">
                <label for="prenom">Ton prénom</label>
                <input v-on:input="toggleResult" v-model="formData.prenom" type="text" id="prenom" class="form-control">
            </div>

            <div class="form-group">
                <label for="txt">Ton texte</label>
                <textarea v-on:input="toggleResult" v-model="formData.txt" id="txt" class="form-control"></textarea>
            </div>



            <!-- Selectboxs -->
            <select  v-model="formData.select" class="mt-3 mb-3" v-on:input="toggleResult">
                <option v-for="(pays, index) in formData.listePays" :key="index">{{pays}}</option>
            </select>




            <!-- Checkboxs -->
            <div class="form-check">
                <input v-model="formData.checkFruits" v-on:input="toggleResult" type="checkbox" id="fraise" value="fraise" class="form-check-input">
                <label for="fraise">Fraise</label>
            </div>

            <div class="form-check">
                <input v-model="formData.checkFruits" v-on:input="toggleResult" type="checkbox" id="pomme" value="pomme" class="form-check-input">
                <label for="pomme">Pomme</label>
            </div>

            <div class="form-check">
                <input v-model="formData.checkFruits" v-on:input="toggleResult" type="checkbox" id="cerises" value="cerises" class="form-check-input">
                <label for="cerises">Cerises</label>
            </div>

            <button @click.prevent="envoiForm" class="btn btn-primary mt-3">Envoyez les données</button>

        </form>

        <br>

        <div v-if="infoSubmit">

            <h2>Résultats</h2>

                <div class="card p-3">
                    <p>Prenom : {{ formData.prenom }}</p>
                    <p style="white-space:pre">Texte : {{ formData.txt }}</p>
                </div>


                <p>Résultats checkboxs</p>
                <ul>
                    <li v-for="(fruit, index) in formData.checkFruits" :key="index">{{fruit}}</li>
                </ul>

                <p>Choix du select : {{formData.select}}</p>


            </div>
       </div>
    
</template>


<script>

export default {
    name: 'Contenu-name',
    data() {
        return {
            formData: {
                prenom: '',
                txt: '',
                checkFruits: [],
                select: '',
                listePays: ['France', 'Guinée', 'Sénégal', 'Canada']
            },
            infoSubmit: false
        }
    },
    methods: {
        envoiForm: function() {
            this.infoSubmit = true;
        },
        toggleResult: function() {
            this.infoSubmit = false;
        }
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