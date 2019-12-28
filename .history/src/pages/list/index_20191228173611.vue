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

  this.recommand = require('@/data/' + option.type + '.json')
  console.log(this.list)
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
