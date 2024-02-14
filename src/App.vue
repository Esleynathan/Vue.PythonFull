<template>
  <TheHeader/>
  <LogarButton/>

</template>

<script>
  import TheHeader from './components/TheHeader.vue';
  import LogarButton from './components/LogarButton.vue';

  export default{
    components: {
      TheHeader,
      LogarButton,
    }
  }
</script>

<style>
  *{
    margin: 0;
    padding: 0;
  }
</style>
