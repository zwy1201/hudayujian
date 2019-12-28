<template>
  <div>

    </div>
</template>

<script>


export default {
  data () {
    return {
     list:[]
      
    }
  },

   onLoad(option){
  console.log(option.type)
  this.recommand = require('@/data/' + option.type + '.json')
  console.log
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
