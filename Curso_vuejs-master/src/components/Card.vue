<template>
  <div class="container">
     <div class="cards">
         <div class="card">
             <img src="https://source.unsplash.com/random/400x400" class="card__header" alt="">
             <article class="card__description">
                 <LikeButton title="Like" v-bind:likeUser="5"/>
                  <LikeButton title="DisLike" v-bind:likeUser="1"/>
                 <p class="descritpion"> 
                     <span class="description">
                         <a href="">#ReactLover</a> 
                     </span>
                     <span class="description">
                        <a href="">#TodosReact</a>

                     </span>
                     </p>
             </article>
        </div>
    
    </div> 
    
    
  </div>
</template>

<script>
import LikeButton from './LikeButton';
export default {

  name: 'Card',
  data: function () {
    return {
      
    }
  },
  components:{
      LikeButton
  },
  methods:{
    
  }
}
</script>