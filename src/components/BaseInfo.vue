<template>
  <section class="base-info mg-tb-30" style="padding-bottom: .1rem;">
  	<rectangle :tip="tip"></rectangle>
  	<ul class="infos font-12 iblk" style="width: 80%">
  		<li v-for="info in infos" class="info iblk mg-b-15">
  			<span style="padding-right: .05rem;" v-html="info.name"></span>:<span style="padding-left: .1rem;">{{info.data}}</span>
  		</li>
  	</ul>
    <img src="../assets/me.jpg" style="width: .9rem;margin-right: 0.4rem;" class="fr">
  </section>
</template>

<script>
import Rectangle from './Rectangle';

export default {
  name: 'baseInfo',
  components: {
    Rectangle
  },
  data () {
    return {
      tip: "基本信息",
      infos: [
      	{
      		name: "姓&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp名",
      		data: "李习凤"
      	},
      	{
      		name: "毕业院校",
      		data: "计算技术研究所"
      	},
      	{
      		name: "电&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp话",
      		data: "13261527720"
      	},
      	{
      		name: "学&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp历",
      		data: "研究生"
      	},
      	{
      		name: "邮&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp&nbsp箱",
      		data: "shuyu_lxf@163.com"
      	},
      	{
      		name: "求职意向",
      		data: "前端开发工程师"
      	}
      ]
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url('../../static/css/common.css');
  .base-info ul li:nth-child(2n+1) {
    width: 55%
  }
  .base-info ul li:nth-child(2n) {
    width: 40%
  }
  .infos{
  	padding: .27rem .05rem 0;
  }
  .info{
  	width: 40%;
  	box-sizing: border-box;
  }
</style>
