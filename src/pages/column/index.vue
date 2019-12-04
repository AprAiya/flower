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
          <image :src="img" style="width:100%" />
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
  </i-grid>
  <i-panel :title="title_name">
    <view style="padding: 15px;">
      <i-card v-for="item in top" :key="item" i-class="split" :extra="item.name" :thumb="item.image">
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
      // title_name: "专栏：市省花",
      // grids: [
      //   {title:"亲情",image:"/static/images/1.png"},
      //   {title:"爱情",image:"/static/images/2.png"},
      //   {title:"友情",image:"/static/images/3.png"},
      //   {title:"其他",image:"/static/images/4.png"}
      // ],
      top: [
        {name:"湖北省",address:"梅花（蔷薇科杏属植物）一般指梅（蔷薇科杏属植物）",image:"/static/images/湖北.jpg",remark:"梅花"},
        {name:"海南省",address:"三角梅一般指叶子花（中央种子目紫茉莉科植物）",image:"/static/images/海南.jpg",remark:"三角梅"},
        {name:"香港",address:"紫荆花（苏木科羊蹄甲属植物）一般指红花羊蹄甲",image:"/static/images/香港.jpg",remark:"紫荆花"},
        {name:"澳门",address:"荷花 属毛茛目睡莲科，是莲属二种植物的通称。",image:"/static/images/澳门.jpg",remark:"荷花"}
      ],
      // imgUrls: [
      // //   'https://images.unsplash.com/photo-1551334787-21e6bd3ab135?w=640',
      // //   'https://images.unsplash.com/photo-1551214012-84f95e060dee?w=640',
      // //   'https://images.unsplash.com/photo-1551446591-142875a901a1?w=640'
      //      "/static/images/5.jpg"
      // ],
      indicatorDots: false,
      autoplay: false,
      interval: 5000,
      duration: 1000
    }
  },

  methods: {
    goType(type){
      console.log(type)
      let url = '../list/main?type=' + type.title
      mpvue.navigateTo({ url })
    }
  },

  created () {
  }
}
</script>

<style scoped>
div >>> .no-border {
  border-width: 0pt;
}
div >>> .split {
  margin-bottom: 10pt;
}
</style>
