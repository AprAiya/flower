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
       title_name: "每周推荐",
         top: [
        {name:"爱情之花",address:"再多一点点距离，我就能靠近你。清晰甜美的空气里，爱你到不能呼吸。",image:"/static/images/f1.jpg",remark:"红玫瑰"},
        {name:"亲情之花",address:"有个地方，是永远可以安然甜睡的港湾，那就是—父母的怀抱。",image:"/static/images/f2.jpg",remark:"康乃馨"},
        {name:"友情之花",address:"我携满天星辰赠你，好教你不逊色人间错落烟火；只有这满天星辰，足够与你相配。",image:"/static/images/f3.jpg",remark:"满天星"},
        {name:"道歉之花",address:"感受生命的豁达和从容，敞开心扉，品味岁月静好，浅笑前行。",image:"/static/images/f4.jpg",remark:"向日葵"},
        {name:"探病之花",address:"真心的祝福，不需要千言万语，只愿你岁岁平安，早日康复！",image:"/static/images/f5.jpg",remark:"百   合"}
        
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

