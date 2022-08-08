<template>
  <div className="tweet">
    <ProfileImage :image="user.image"/>
    <div className="body">
      <div className="top">
        <User :userData="user"/>
        <Timestamp :timestamp="timestamp"/>
      </div>
      <Message :message="message" :edit="edit"/> 
       <Actions @like2="like3" /> 

    </div> 

    <i class="fas fa-ellipsis-h" @click="dots1"></i>
  </div>
</template>

<script>
import ProfileImage from './ProfileImage.vue'
import User from "./User.vue"
import Timestamp from './Timestamp.vue'
import Message from './Message.vue'
import Actions from "./Actions.vue"

export default {
  components: {
    ProfileImage,
    User,
    Timestamp,
    Message,
    Actions
  },
  props: {
    user: Object,
    timestamp: String,
    message: String,
    edit: Boolean  

  },
  //mounted() {
    //console.log(this.user);
  //},
  methods: {
    like3() {
      this.$emit("like4");
    },
    dots1() {
      this.$emit("dots2");
    }
  }
}
</script>


<style scoped>
a {
  color: #42b983;
}
</style>