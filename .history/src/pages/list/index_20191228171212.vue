<template>
  <div>

    </div>
</template>

<script>


export default {
  data () {
    return {
     
      
    }
  },

   onLoad(option){
  console.log(option.type)
  this.recommand = require('@/data/' + option.type + )

   },
  methods: {
  
  },

  created () {
    // let app = getApp()
  }
}
</script>

<style scoped>

</style>
