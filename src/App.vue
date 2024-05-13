<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader,
  },
  data() {
    return {
    };
  },
}
</script>


<template>
    <header>

    

      <AppHeader 
        :links="links"
      
      />
    </header>


</template>

<style scoped>

</style>