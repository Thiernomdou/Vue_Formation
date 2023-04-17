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

            <h2>Résultats</h2>

            <div class="card p-3">
                <p>Prenom : {{ formData.prenom }}</p>
                <p style="white-space:pre">Texte : {{ formData.txt }}</p>
            </div>

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
                txt: ''
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