<template>
    <div>
        <p>Python Full</p>
        <hr>
        <ListaModulos v-if="exibirModulo" @fecharFilho="fechar()" :modulos="lmodulos"/>

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
                lmodulos: ['Introdução ao Python', 'Django', 'Banco de dados'],
                curso: 'Python Full',
                exibirModulo: true,
            }
        },
        methods:{
            fechar(){
                this.exibirModulo = !this.exibirModulo
            }
        }
    }
</script>