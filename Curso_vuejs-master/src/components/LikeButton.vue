<template>
    <button class="button" @click="like">
        {{title}} {{likeUser}}
    </button>
</template>

<script>
export default {
  name: 'LikeButton',
  data: function () {
    return {
      count: 0,
      userVote: false
    }
  },
  props:{
      title:String,
      likeUser:Number
  },
  methods:{
      like:function(){
          if(!this.userVote){
              this.userVote=true;
                this.likeUser ++;
          }else{
              this.userVote=false;
              this.likeUser --;
          }
      }
  }
}
</script>