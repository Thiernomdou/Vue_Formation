<template>
    <div>   
        <ul class="liste">
            <li v-for="(fruit, index) in fruits" v-bind:key="index">{{ fruit }}</li>
        </ul>
        <p>{{ prenom.nom }}</p>

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
        props: {
            prenom: {
                type: Object
            }
        }
    }
</script>

<style scoped src="./Liste-fruits.css">

</style>