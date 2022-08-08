<template>
      <div className="actions">
      <i class="far fa-comment"></i>
      <i class="fas fa-retweet"></i>
      <i class="far fa-heart" :class="{active: isActive}" @click="like1"></i>
      <i class="fas fa-share"></i>
    </div>
</template>

<script>
export default {
    data() {
        return {
            isActive: false,
            liked: ""
        }
    },
    methods: {
        like1() {
            this.$emit("like2");
            this.isActive = !this.isActive;
           
        }
    }
  
   

}
</script>

<style>

</style>