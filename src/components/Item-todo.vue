<template>

    <div>
        <div class="card my-2 item-todo">
            <p>{{ tache }}</p>
            <div @click="suppression" class="btn btn-danger btn-supr">X</div>
        </div>
    </div>

</template>

<script>


export default {
    name: 'Item-todo',
    props: ['tache', 'suppression']

}

</script>

<style scoped>

    .item-todo {
        position: relative;
        padding: 20px 60px 20px 30px;
        font-size: 20px;
        height: 88px;
    }
    .btn-supr {
        position: absolute;
        top: 10px;
        right: 10px;

    }
    .item-todo p {
        margin-bottom: 0!important;
    }

</style>
