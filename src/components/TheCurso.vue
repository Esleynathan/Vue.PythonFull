<template>
    <div>
        <p>Python Full</p>
        <hr>
        <ListaModulos :modulos="lmodulos"/>

    </div>

</template>

<script>
    import ListaModulos from './ListaModulos.vue';

    export default {
        components: {
            ListaModulos
        },
        data(){
            return{
                lmodulos: ['Introdução ao Python', 'Django', 'Banco de dados']
            }
        }
    }
</script>