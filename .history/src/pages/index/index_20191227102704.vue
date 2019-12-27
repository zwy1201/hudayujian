<template>
  <div>
    <i-grid i-class="no-border">
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/1.png" />
        </i-grid-icon>
        <i-grid-label>小黄车</i-grid-label>
    </i-grid-item>
    
    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/2.png" />
        </i-grid-icon>
        <i-grid-label>小蓝车</i-grid-label>
    </i-grid-item>

    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/3.png" />
        </i-grid-icon>
        <i-grid-label>摩拜</i-grid-label>
    </i-grid-item>

    <i-grid-item i-class="no-border">
        <i-grid-icon>
            <image src="/static/images/4.png" />
        </i-grid-icon>
        <i-grid-label>租八戒电动车</i-grid-label>
    </i-grid-item>
    </i-grid>

 <i-panel title="">
    <view style="padding: 15px;">PANEL 内容区域</view>
</i-panel>

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
div >>> .no-border{
  border-width:0pt;
}
div >>> .split{
  margin-bottom:10pt;
}
</style>
