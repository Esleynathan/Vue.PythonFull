<template>
    <ul>
        <li v-for="(item, index) in modulos" :key="index">
            {{item}}
        </li>
    </ul>
</template>

<script>
    export default {
        props: ['modulos']
    }
</script>