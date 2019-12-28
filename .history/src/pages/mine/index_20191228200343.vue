<template>
  <div>

<open-data type="userAvatarUrl"></open-data>

    </div>
</template>

<script>


export default {
  data () {
    return {
     
      
    }
  },

  components: {
    card
  },

  methods: {
  
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>
.userinfo {
  position: relative;
  width: 750rpx;
  height: 320rpx;
  color: #666;
  display: flex;
  flex-direction: column;
  align-items: center;
}
 
.userinfo-avatar {
  overflow:hidden;
  display: block;
  width: 160rpx;
  height: 160rpx;
  margin: 20rpx;
  margin-top: 50rpx;
  border-radius: 50%;
  border: 2px solid #fff;
  box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
}
</style>
