<template>
    <div class="bloc-modale" v-if="revele">

        <div class="overlay" @click="toggleModale"></div>

        <div class="card modale">
            <div class="btn btn-danger btn-modale" @click="toggleModale">X</div>
            <h2>Le contenu de la modale</h2>
        </div>

    </div>
</template>

<script>

export default {
    name: 'Modale-text',
    props: ['revele', 'toggleModale']
}

</script>


<style>

.bloc-modale {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
}

.overlay {
    background: rgba(0,0,0,0.5);
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0; 
}
.modale {
    background: #f1f1f1;
    color: #333;
    padding: 50px;
    position: fixed;
    bottom: 10%;
}
.btn-modale {
    position: absolute;
    top: 10px;
    right: 10px;
}
</style>