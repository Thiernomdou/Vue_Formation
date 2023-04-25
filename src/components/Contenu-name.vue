<template>

    <div class="container mt-5">
        <h1>Notre premier Formulaire</h1>
       
       
        <form>


            <div class="form-group">
                <label for="prenom">Ton prénom</label>
                <input v-model="formData.prenom" type="text" id="prenom" class="form-control">
            </div>

            <div class="form-group">
                <label for="txt">Ton texte</label>
                <textarea v-model="formData.txt" id="txt" class="form-control"></textarea>
            </div>



            <div class="form-check">
                <input v-model="formData.checkFruits" type="checkbox" id="fraise" value="fraise" class="form-check-input">
                <label for="fraise">Fraise</label>
            </div>

            <div class="form-check">
                <input v-model="formData.checkFruits" type="checkbox" id="pomme" value="pomme" class="form-check-input">
                <label for="pomme">Pomme</label>
            </div>

            <div class="form-check">
                <input v-model="formData.checkFruits" type="checkbox" id="cerises" value="cerises" class="form-check-input">
                <label for="cerises">Cerises</label>
            </div>



            <h2>Résultats</h2>

            <div class="card p-3">
                <p>Prenom : {{ formData.prenom }}</p>
                <p style="white-space:pre">Texte : {{ formData.txt }}</p>
            </div>


            <p>Résultats checkboxs</p>
            <ul>
                <li v-for="(fruit, index) in formData.checkFruits" :key="index">{{fruit}}</li>
            </ul>

        </form>


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
                checkFruits: []
            }
        }
    },
    methods: {
        
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