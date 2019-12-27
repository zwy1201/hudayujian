<template>
  <div>
    <i-grid i-class="no-border">
    <i-grid-item  i-class="no-border">
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

 <i-panel ：title="title_name">
    <view style="padding: 15px;">
      <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
    <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
    <i-card i-class="split" title="卡片标题" extra="额外内容" thumb="https://i.loli.net/2017/08/21/599a521472424.jpg">
    <view slot="content">内容不错</view>
    <view slot="footer">尾部内容</view>
</i-card>
    </view>
</i-panel>


    </div>
</template>

<script>


export default {
  data () {

    return {
     title_name:"空闲",
     grids:[
       {
            title:"小黄车",image:"/static/images/1.png",
            title:"小蓝车",image:"/static/images/2.png",
            title:"摩拜",image:"/static/images/3.png",
            title:"租八戒电动车",image:"/static/images/4.png"
       }
     ]
      
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
