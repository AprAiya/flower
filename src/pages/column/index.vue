<template>
  <div>

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
       title_name: "专栏：市省花",
         top: [
        {name:"湖北省",address:"梅花（蔷薇科杏属植物）一般指梅（蔷薇科杏属植物）",image:"/static/images/Hubei.jpg",remark:"梅花"},
        {name:"海南省",address:"三角梅一般指叶子花（中央种子目紫茉莉科植物）",image:"/static/images/hainan.jpg",remark:"三角梅"},
        {name:"香港",address:"紫荆花（苏木科羊蹄甲属植物）一般指红花羊蹄甲",image:"/static/images/HongKong.jpg",remark:"紫荆花"},
        {name:"澳门",address:"荷花 属毛茛目睡莲科，是莲属二种植物的通称。",image:"/static/images/Macao.jpg",remark:"荷花"}
      ],
    }
  },

  methods: {
  },

  created () {
  }
}
</script>

<style scoped>
</style>

