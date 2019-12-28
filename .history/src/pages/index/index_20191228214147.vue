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
        '5.png',
        '6.',
        'http://www.canyin88.com/uploads/190415/99ad8154e7332ca96ccb323580b3b8a2_3.jpg'
      ],
      indicatorDots: true,
      autoplay: true,
      interval: 5000,
      duration: 1000,

     grids:[
       
            {title:"小黄车",image:"/static/images/1.png",url:'../list/main?type=1'},
            {title:"小蓝车",image:"/static/images/2.png",url:'../list/main?type=2'},
            {title:"摩拜",image:"/static/images/3.png",url:'../list/main?type=3'},
            {title:"租八戒电动车",image:"/static/images/4.png",url:'../list/main?type=4'}
       
     ],
     recommand: top
    }
   
  },

  components: {
    card
  },

  methods: {
    goList (url) {
      mpvue.navigateTo({ url })
    },
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

