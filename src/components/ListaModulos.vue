<template>
    <div>
        <button @click="fecharFilho()">
            Fechar
        </button>
        <ul>
            <li v-for="(item, index) in modulos" :key="index">
                {{item}}
            </li>
        </ul>
    </div>

</template>

<script>
    export default {
        props: {
            modulos: {
                type: Array,
                required: true,
            },
            nome: {
                type: String,
            }
        },
        methods:{
            fecharFilho(){
                this.$emit('fecharFilho')
            }
        }
    }
</script>