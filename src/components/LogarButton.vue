<template>
    <span> {{isAluno}}</span>
</template>

<script>
export default {
    data() {
        return {
            usuario: {
                nome: 'Caio Sampaio',
                cursos: [
                'Python Full',
                'Vue Full'
            ]
        }
    }
    },

    methods: {

    },

    computed: {
        isAluno(){
            return this.usuario.cursos.length > 0 ? 'Já é aluno' : 'Não é aluno'
        }
    }
};
</script>

<style scoped>
    button{
        border: none;
        padding: 10px;
        background-color: aqua;
        color: black;
    }
</style>