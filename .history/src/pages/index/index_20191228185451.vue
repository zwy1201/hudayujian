<template>
  <div>
     <swiper
      :indicator-dots="indicatorDots"
        :autoplay="autoplay" 
        :interval="interval" 
        :duration="duration"
        >
        <block v-for="img in imgUrls" :key="img">
          <swiper-item>
            <image :src="item" style= width="355"></view>
          </swiper-item>
        </block>
      </swiper>
    <i-grid i-class="no-border">
    <i-grid-item @click="goType(grid)" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
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
      <i-card  v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.iamge">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">{{item.address}}</view>
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
       
            {title:"小黄车",image:"/static/images/1.png"},
            {title:"小蓝车",image:"/static/images/2.png"},
            {title:"摩拜",image:"/static/images/3.png"},
            {title:"租八戒电动车",image:"/static/images/4.png"}
       
     ],
     top:[
       {name:"编号1",address:"地址1",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍1" },
       {name:"编号2",address:"地址2",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍2" },
       {name:"编号3",address:"地址3",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍3" },
       {name:"编号4",address:"地址4",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍4" }
     ]
    
    }
  },

  components: {
    card
  },

  methods: {
    goType(type){
        console.log(type)
        let url = '../list/main?type=' + type.title
        mpvue.navigateTo({ url })
    }
  
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
