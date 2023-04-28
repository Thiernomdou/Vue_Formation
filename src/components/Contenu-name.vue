<template>

    <div class="container mt-5">

        <h1>Rentrez vos choses à faire</h1>

        <form>

            <div class="form-group">
                <label for="action">Action</label>
                <input v-model="formData.tache" type="text" class="form-control" id="action">
            </div>
            <button @click.prevent="creationItem" class="btn btn-primary mt-2 mb-3">Créer une tâche</button>

        </form>

        <ul>
            <li v-for="(tache, index) in tableauTaches" :key="index">
                <Item-todo :tache="tache" :id="index" :suppression="suppression"></Item-todo>
            </li>
        </ul>

    </div>
    
</template>


<script>

import ItemTodoVue from './Item-todo.vue'


export default {
    name: 'Contenu-name',
    components: {
        'Item-todo': ItemTodoVue
    },
    data() {
        return {
            formData: {
                tache: ''
            },
            tableauTaches: ['JavaScript', 'Vue', 'React', 'Angular']
        }
    },
    methods: {
        creationItem: function() {
            this.tableauTaches.push(this.formData.tache);
            this.formData.tache = '';
        },
        suppression: function(e) {
            console.log(e.target.parentNode.id);
            // this.tableauTaches.splice(e.target.parentNode.id, 1);
        }
    }
}

</script>

<style>

h1 {
    margin-top: 100px!important;
}
ul {
    list-style-type: none;
    padding: 0;
}


</style>