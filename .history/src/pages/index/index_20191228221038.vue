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
            <image :src="img" style="width：100%" />
          </swiper-item>
        </block>
      </swiper>

	   <i-grid i-class="no-border">
    <i-grid-item  @click="goType(grid)" v-for="grid in grids" :key="grid" i-class="no-border">
        <i-grid-icon>
            <image :src="grid.image" />
        </i-grid-icon>
        <i-grid-label>{{grid.title}}</i-grid-label>
    </i-grid-item>
</i-grid>

 <i-grid i-class="no-border">
    <i-grid-item @click="goType(krid)" v-for="krid in krids" :key="krid" i-class="no-border">
        <i-grid-icon>
            <image :src="krid.image" />
        </i-grid-icon>
        <i-grid-label>{{krid.title}}</i-grid-label>
    </i-grid-item>
  </i-grid>

 <i-panel ：title="title_name">
    <view style="padding: 15px;">
       <i-card  v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.iamge">
    <view slot="content">{{item.remark}}</view>
    <view slot="footer">{{item.content}}</view>
</i-card>
      
    </view>
</i-panel>
</div>
</template>


<script>


export default {
  data () {

    return {
     grids:[
       
            {title:"小黄车",image:"/static/images/1.png"},
            {title:"小蓝车",image:"/static/images/2.png"},
            {title:"摩拜",image:"/static/images/3.png"},
            {title:"租八戒电动车",image:"/static/images/4.png"}
       
     ],
     krids:[
            {title:"小黄车1",image:"/static/images/5.png"},
            {title:"小蓝车2",image:"/static/images/2.png"},
            {title:"摩拜3",image:"/static/images/3.png"},
            {title:"租八戒电动车4",image:"/static/images/4.png"}
       
     ],
      imgUrls: [
      'https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640',
      'https://images.unsplash.com/photo-1551214021-84f95e060dee?w=640',
      'https://images.unsplash.com/photo-1551446591-142875a901a1?w=640'
    ],
    indicatorDots: false,
    autoplay: false,
    interval: 5000,
    duration: 1000
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


 
      