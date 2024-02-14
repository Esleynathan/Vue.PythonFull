<template>
    <div>
        <p>Mensagens</p>
        <div id="mensagens">

        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            novaMensagem: ""
        }
    },

    methods: {
        gerarStringAleatoria() {
            const letras = 'abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ';
            let resultado = '';
            for (let i = 0; i < 10; i++) {
            resultado += letras.charAt(Math.floor(Math.random() * letras.length));
            }
            return resultado;
        },

        addMessage(){
            this.mensagens = document.getElementById('mensagens')
            this.mensagens.innerHTML += '<span>' + this.novaMensagem + '</span><hr>'
        }

    },

    watch: {
        novaMensagem(){
            this.addMessage();
        }
    },

    mounted(){
        setInterval(() => {
            this.novaMensagem = this.gerarStringAleatoria();
        }, 5000);        
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