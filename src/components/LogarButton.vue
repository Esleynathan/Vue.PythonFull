<template>
    <div v-if="local === 'materiais'"> Você esta nos materiais</div>
    <div v-else-if="local === 'sobre'"> Você esta no sobres</div>
    <div v-else> Você esta no duvidas</div>
    <hr>
    <br>
    <br>

    <div 
    v-for="(curso, index) in cursos"
    v-bind:key="curso.nome"
    >   
        <p>{{ index }}</p>
        <p>{{ curso.nome }}</p>
        <p>{{ curso.qtdAulas }}</p>
        <p>{{ curso.duracao }}</p>
        <hr>
    </div>


</template>

<script>
    export default{
        data(){
            return {
                local: 'sobre',
                cursos: [
                    {
                        nome: 'Python full',
                        qtdAulas: '600',
                        duracao: '110',                    
                    },
                    {   nome: 'Vue full',
                        qtdAulas: '100',
                        duracao: '18',                    
                    },
                    {   nome: 'IA full',
                        qtdAulas: '400',
                        duracao: '20',                    
                    },
                ],
            }
        }

    }

</script>

<style scoped>
    button{
        border: none;
        padding: 10px;
        background-color: aqua;
        color: black;
    }
</style>