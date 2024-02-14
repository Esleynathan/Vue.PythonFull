<template>
    <header id="MeuHeader"> 
        <p>{{nomeEmpresa}} - CNPJ: {{cnpj}}</p>
    </header>
</template>

<script>
    export default{
        data(){
            return{
                cnpj: '',
                nomeEmpresa: ''
            }
        },
        created(){
            this.cnpj = '76.717.248/0001-30'
            this.nomeEmpresa = 'Pythonando'
        },
        mounted(){
            console.log(document.getElementById('MeuHeader'))
        }

    }
</script>

<style scoped>
    header{
        background-color: #222222;
        color: white;
        padding: 20px;
    }

</style>