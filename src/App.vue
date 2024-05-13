<script>
import AppHeader from './components/AppHeader.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppFooter,

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
    <main>

    </main>
    <footer>
      <AppFooter></AppFooter>
    </footer>


</template>

<style scoped>

</style>