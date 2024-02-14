<template>
    <div v-if="local === 'materiais'"> Você esta nos materiais</div>
    <div v-else-if="local === 'sobre'"> Você esta no sobres</div>
    <div v-else> Você esta no duvidas</div>
    <hr><br>

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
    <br>

    <input placeholder="Pontos" :value="pontos">
    <button v-on:click="contar()">Soma 10</button>
    <hr><br>

    <input v-model="contador" placeholder="Pontos">
    <p> O valor é: {{contador}}</p>
    <hr><br>

    <select v-model="curso">
        <option value="pf">Python Full</option>
        <option value="vf">Vue Full</option>
    </select>
    O valor é: {{ curso }}
    <hr><br>

    <button @click.stop="clickButton">
        Button
    </button>
    <hr><br>

    <a @click.prevent="click" href="https://plataforma.pythonando.com.br">Clique aqui.</a>

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
                pontos: 0,
                contador: '100',
                curso: 'pf',
                counter: 0,
            }
        },
        methods: {
            contar(){
                this.pontos = this.pontos + 10
            },
            clickButton(){
                console.log('Click no botão')
            },
            clickDiv(){
                console.log('Click no div')
            },
            click(){
                console.log('Fui Chamado')
                window.location.href = "https://plataforma.pythonando.com.br"
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