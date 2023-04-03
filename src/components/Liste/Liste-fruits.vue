<template>
    <div>   
        <ul class="liste mt-5">
            <li v-for="(film, index) in myArr" v-bind:key="index">
                <div class="card">
                    <div class="card-body">
                        Titre: {{ film.titre }}
                        <br>
                        Date:  {{ film.date }}
                    </div>
                </div>
            </li>
        </ul>
        <p>{{ txt }}</p>
        <div @click="supprFilm" class="btn btn-danger mt-2">Supprimer le film</div>
        <div @click="supprTxt" class="btn btn-danger mt-2 ml-2">Supprimer le texte</div>
        <div @click="changeTitre" class="btn btn-danger mt-2 ml-2">Modifie le Titre</div>

    </div>
</template>

<script>
    export default {
        name: 'Liste-fruits',
        data() {
            return {
                fruits : ["Tomate", "Papaye", "Mangue"]
            }
        },
        methods: {
            supprFilm: function() {
                this.myArr 
            },
            supprTxt: function() {
                this.txt
            },
            changeTitre: function() {
                //le nom de l'évènement que le parent peut écouter en premier paramètre le l'emit et le second est ce qu'on a envie de lui passer
                this.$emit('changeTitre', 'Mon nouveau Titre')
            }
        },
        props: ['myArr', 'txt']
    }
</script>

<style scoped src="./Liste-fruits.css">

</style>