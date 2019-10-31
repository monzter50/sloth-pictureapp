<template>
  <div id="app">
   <!-- <LikeButton/> -->
   <Card/> 
    <router-view/>
  </div>
</template>

<script>

// import LikeButton from './components/LikeButton';
import Card from './components/Card';
export default {
  name: "App",
  components: {
    Card
  },
  data(){
    return{
      items:null,
       error:false,
      loading:true,
    }
  },
  methods:{
    getData(){
      let that= this;
        fetch(`https://api.instagram.com/v1/users/self/media/recent/?access_token=${process.env.VUE_APP_TOKEN}`)
        .then(response => response.json())
        .catch(error => 
            this.error = true
        )
        .then(response => 
            that.items = response.data
            
        ).finally(() => this.loading = false);
          console.log('Success:', this.items)
    }
  },
  created(){
    this.getData();
  }
}
</script>
