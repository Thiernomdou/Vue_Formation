<template>
    <div>
        <p>{{ txt }}</p>
        <liste v-bind:prenom="prenom"></liste>
    </div>
    
</template>


<script>
import Liste from './Liste/Liste-fruits.vue'

export default {
    name: 'Contenu-name',
    data() {
        return {
            txt : 'Je suis le contenu',
            prenom: "Thierno"
        }
    },
    components: {
        'liste': Liste
    }
}

</script>