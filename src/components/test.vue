<template>
    <div v-if="show">
      111111111
    </div>
</template>

<script>
  export default {
    name: 'test',
    data(){
      return{
        show:false
      }
    },
    created () {
      this.show=true;
      console.log(2222222222)
    },
    watch:{
      $route(){
        this.show=false;
        this.$nextTick(v=>{
          this.show=true;
          console.log(7777777)
        })
      }
    }
  }
</script>

<style scoped>

</style>
