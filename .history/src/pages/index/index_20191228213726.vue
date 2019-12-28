	<template>
                <div>
<swiper
      :indicator-dots="indicatorDots"
        :autoplay="autoplay" 
        :interval="interval" 
        :duration="duration"
        >
<block v-for="item in imgUrls" :key="item">
      <swiper-item>
        <image :src="item" style="width:100%;"/>
      </swiper-item>
    </block>
  </swiper>

 <i-grid i-class="no-border">
      <i-grid-item @click="goList(item.url)" i-class="no-border" v-for="item in grids" :key="item">
          <i-grid-icon>
              <image :src="item.img" />
          </i-grid-icon>
          <i-grid-label>{{item.type}}</i-grid-label>
      </i-grid-item>
  </i-grid>


   <i-panel title="强烈推荐">
    <view>
      <i-card @click="goType(item.type)" i-class="split" v-for="item in recommand" :key="item" :extra="item.name" :thumb="item.img">
          <view slot="content">推荐理由：{{item.remark}}</view>
          <view slot="footer">地址：{{item.address}}</view>
      </i-card>
    </view>
  </i-panel>
  </div>
</template>


<script>
import card from '@/components/card'
import top from '@/data/top.json'

export default {
  data () {

    return {
      imgUrls: [
        'http://www.canyin88.com/uploads/image/2019/04/16/1555378220872933.jpg',
        'http://www.canyin88.com/uploads/image/2019/04/15/1555321255843942.jpg',
        'http://www.canyin88.com/uploads/190415/99ad8154e7332ca96ccb323580b3b8a2_3.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000,

     grids:[
       
            {title:"小黄车",image:"/static/images/1.png",url:'../list/main?type=1'},
            {title:"小蓝车",image:"/static/images/2.png",url:'../list/main?type=2'},
            {title:"摩拜",image:"/static/images/3.png",url:'../list/main?type=1'},
            {title:"租八戒电动车",image:"/static/images/4.png",url:'../list/main?type=1'}
       
     ],
     top:[
       {name:"编号1",address:"地址1",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍1" },
       {name:"编号2",address:"地址2",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍2" },
       {name:"编号3",address:"地址3",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍3" },
       {name:"编号4",address:"地址4",image:"https://i.loli.net/2017/08/21/599a521472424.jpg",remark:"介绍4" }
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

