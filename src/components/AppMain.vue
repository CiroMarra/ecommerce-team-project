<script>
export default {
  name: 'AppMain',
  components:{
  },
  data() {
    return {

    };
  },
  mounted() {
    console.log(this.imageUrls);
  }
}
</script>

<template>
    <section class="ms-bg-section">
        <div class="container position-relative">
            <div class="box-img">
                <img v-for="(imageUrl, index) in imageUrls" :key="index" :src="imageUrl" alt="" class="mx-4 py-3 px-2">
            </div>
            
        </div>
    </section>

</template>

<style scoped>
 .ms-bg-section {
    background-color: #191935;
    height: 40vw;
    color: white;
 }


 .box-img {
    background-color: #202046;
    height: 200px;
    width: 1230px;
    position: absolute;
    bottom: -100px;
    left: 40px;
 }
</style>