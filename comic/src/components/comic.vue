<template>
  <div class="container">
    
    <h2 id="titleComic">{{obj.title}}</h2>
    <div id="image" v-bind:style="{ backgroundImage:'url('+obj.url+')' }"></div>

     <rating :grade="3" :maxStars="5" :hasCounter="true" />
  </div>
</template>

<script>
import axios from 'axios'
import rating from '@/components/rating.vue'
export default {
  name: 'comic',
  components: {
    
    rating
  },
data() {   
      return {
         dataComic: [],
          obj: []
      }
    },

    methods: {
     
    },

    mounted(){  
     let vueHome = this;      
      
      axios.get("https://jsonplaceholder.typicode.com/photos?albumId=80")
      .then(function (response){
        vueHome.dataComic = response.data;        
        const idx = Math.floor(Math.random() * vueHome.dataComic.length);
        console.log('ramdom');
        console.log(vueHome.dataComic[idx]);
        
         vueHome.obj= vueHome.dataComic[idx]
      })
    },
    
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">

</style>
