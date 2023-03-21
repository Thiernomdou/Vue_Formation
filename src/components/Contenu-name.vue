<template>
    <div>
        <p>{{ txt }}</p>
        <liste></liste>
    </div>
    
</template>


<script>
import Liste from './Liste/Liste-fruits.vue'

export default {
    name: 'Contenu-name',
    data() {
        return {
            txt : 'Je suis le contenu'
        }
    },
    components: {
        'liste': Liste
    }
}

</script>