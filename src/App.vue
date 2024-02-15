<template>
  <TheHeader/>
  <LogarButton/>
  <TheCurso/>

</template>

<script>
  import TheHeader from './components/TheHeader.vue';
  import LogarButton from './components/LogarButton.vue';
  import TheCurso from './components/TheCurso.vue';

  export default{
    components: {
    TheHeader,
    LogarButton,
    TheCurso
}
  }
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
</style>
