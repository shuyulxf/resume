<template>
  <div>
    <section class="education">
        <rectangle bg="true" :tip="education.tip"></rectangle>
        <ul class="infos mg-tb-30">
          <li class="info mg-b-15" v-for="info in education.edus">
            <span class="iblk w-33">{{info.time}}</span><span class="iblk w-33">{{info.school}}</span><span class="iblk w-33">{{info.edu}}</span>
          </li>
        </ul>
    </section>
    <section class="experience">
        <rectangle bg="true" :tip="experience.tip"></rectangle>
        <ul class="infos mg-tb-30">
          <li v-for="info in experience.exps" style="padding-bottom: .15rem;">
            <span class="iblk w-33" style="padding-bottom: .1rem">{{info.title.time}}</span><span class="iblk w-33" style="padding-bottom: .1rem">{{info.title.cnt}}</span><span class="iblk w-33" style="padding-bottom: .1rem">{{info.title.pos}}</span>
            <ul class="lists">
              <li v-for="list in info.lists">{{list}}</li>
            </ul>
          </li>
        </ul>
    </section>
    <section class="skills" style="padding-bottom: .1rem;">
      <rectangle bg="true" :tip="skills.tip"></rectangle>
      <ul class="infos mg-tb-30 lists">
        <li v-for="list in skills.lists" >{{list}}</li>
      </ul>
    </section>
    <section class="reward">
      <rectangle bg="true" :tip="rewards.tip"></rectangle>
      <ul class="infos mg-tb-30">
        <li v-for="list in rewards.lists">
            <span class="iblk w-33" style="padding-bottom: .1rem">{{list.time}}</span><span class="iblk w-33" style="padding-bottom: .1rem">{{list.reward}}</span>
        </li>
      </ul>
    </section>
    <section class="certificate">
        <rectangle bg="true" :tip="certificate.tip"></rectangle>
        <ul class="infos mg-tb-30" style="padding-bottom: .1rem;">
          <li v-for="list in certificate.lists">
            {{list}}
          </li>
        </ul>
    </section>
    <section class="selfEvaluation">
      <rectangle bg="true" :tip="selfEvaluation.tip"></rectangle>
      <ul class="infos mg-tb-30 lists">
          <li v-for="list in selfEvaluation.lists">
            {{list}}
          </li>
        </ul>
    </section>
  </div>
</template>

<script>
import Rectangle from './Rectangle';
export default {
  name: 'detailInfo',
  components: {
    Rectangle
  },
  data () {
    return {
      education: {
        tip: "教育背景",
        edus: [
          {
            time  : "2014.09-2018.07",
            school: "计算技术研究所",
            edu   : "硕士(计算机技术)"
          },
          {
            time  : "2010.09-2014.07",
            school: "北京邮电大学",
            edu   : "本科(计算机科学与技术"
          }
        ]
      },
      experience: {
        tip: "项目经验",
        exps: [
          {
            title: {
              time: "2016-04 至今",
              cnt : "中国电信智能客服机器人",
              pos : "项目接口人和 WEB 开发"
            },
            lists: [
              "作为导师公司和电信集团智能客服机器人合作项目的接口人，主要负责将电信集团提出的部分需求分配到的相应的人，并把控需求进度",
              "智能客服机器人网站前端和后台的开发和维护，包括三个版本 PC 版兼容ie8+、手机版、实体机器人版，手机版嵌入安卓 app，前端主要使用 jQuery 库",
              "智能客服机器人的全国推广，撰写对接规范文档，嵌入全国各个省份的应用渠道",
              "电信集团的机器人端的推广活动，开发活动页，包括前端和后端，保证高并发下的数据一致性，并将活动可配置化，减少线上活动的维护成本",
              "智能客服机器人首页多媒体知识配置后台的开发，使用技术:前端使用基于 react 框架的前端组件库ant-design、后台结合 j2ee 中的 servlet、struct 等技术、数据库使用 oracle",
              "智能客服机器人意见统计、pv 量统计、活动中奖记录统计、活动流量统计、个人信息接口调用记录等后台数据统计页面的开发和维护。技术:前端基于 jquery、jquery.cookie、art-template 前端模板，、后台结合j2ee 中的 servlet、struct 等技术、数据库使用 oracle",
              "实体机器人页面的开发和维护，作为技术支持出差提供技术支持",
              "知识管理系统(KM)交互模块的新需求开发。使用技术:前端使用 easyUI 框架",
              "活动配置模块的开发，收集集团活动需求，结合现行工作流引擎、zookeeper 等技术，实现各个活动公共模块的配置。"
            ]
          },
          {
            title: {
              time: "2015-11",
              cnt : "移动端静态页面开发",
              pos : ""
            },
            lists: [
              "完成多个移动端响应式静态页面的开发，高度还原设计稿，使用 rem 实现移动端的响应式开发"
            ]
          },
          {
            title: {
              time: "2014-12 至 2015-01",
              cnt : "基于微擎的二次开发",
              pos : ""
            },
            lists: [
              "了解用户需求，基于微擎系统后台，实现婚礼宣传页配置、参加活动的新人信息展示和数据管理后台的开发",
              "熟悉微擎系统后台架构，研读原有项目代码",
              "婚礼宣传页信息在微擎后台可以实现配置",
              "信息展示页面实现展示，排序，报名，投票等功能",
              "应用到的技术,后台:php+mysql 前端:bootstrap"
            ]
          },
          {
            title: {
              time: "2012-08 至 2013-05",
              cnt : "文档转换工具",
              pos : "项目参与者(项目规模: 4 人)"
            },
            lists: [
              "简介: 该项目是学校和 IBM 公司的校企合作项目。主要是识别文档中的元素，包括目录、标题、段落、列 表、表格等，并为其添加标签，从而把已定义格式的文档转换为带有相应标签的文档。标签 bookmaster 为 IBM 内部标签，用来标记文档各省，且 IBM 公司存在将带有标签的文档转换为正确文档格式的软件。但带标签的文档需要手动添加，而该项目就是为了解决这个问题，由程序为文档添加 bookmaster 标签",
              "技术:C++、MFC",
              "责任:参与需求分析，并写文档 实现文档转换的部分代码编写，包括软件底层的编写，实现目录、标题等文档元素标签的添加，软件 logo 设计等。"
            ]
             
          }
        ]
      },
      skills: {
        tip: "专业技能",
        lists: [
          "熟悉 HTML、CSS、JavaScript、nodeJS 等基本技术，熟悉 http 协议",
          "熟悉 Sea.js、require.js 等模块化开发框架，研读过 SeaJs 源码，熟悉实现原理",
          "熟悉 Backbone 前端 MVC 框架，研读过源码",
          "熟悉 art-template 等前端模板，研读过源码，熟悉其实现原理",
          "熟悉 jQuery、Zepto、underscore、reactjs、vuejs 等框架，研读过 jquery、underscore、vue 源码",
          "熟悉 Bootstrap、easyUI、Ant Design 等前端 UI 框架, 研读过 Bootstrap 部分源码",
          "熟悉 webpack、fis、gulp 等前端构建工具",
          "熟悉 php 语言以及 MVC 框架 yaf",
          "熟悉 java 语言以及 Java WEB 开发相关技术，如 structs、servlet、Spring、Spring MVC 等",
          "熟悉数据库原理以及 mysql、sql server、oracle 等数据库",
          "熟悉数据结构和基本算法",
          "了解 tomcat、httpd 等 web 网络服务器",
          "了解 linux 系统、熟练使用 linux 基本命令"
        ]
      },
      rewards: {
        tip: "获奖情况",
        lists: [
          {
            time: "2013 年 9 月",
            reward: "励志奖学金"
          },
          {
            time: "2012 年 9 月",
            reward: "北京邮电大学二等奖学金"
          },
          {
            time: "2011 年 9 月",
            reward: "北京邮电大学三等奖学金"
          }
        ]  
      },
      certificate: {
        tip: "技能证书",
        lists:[
          "大学英语六级(CET-6)，良好的听说读写能力，快速浏览英语专业文件及书籍"
        ]
      },
      selfEvaluation: {
        tip: "自我评价",
        lists: [
          "认真负责，吃苦耐劳，研究生期间，为了项目上的事情，经常半夜查问题。",
          "性格开朗，善于沟通，负责过项目的协调工作，并完成了电信的智能客服的多个渠道和全国大部分省份对接工作。",
          "热爱 WEB 开发，对前后端都有涉猎，可以独立完成中小型站点的开发和部署。"
        ]
      }
    }
  },
  computed: {
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  @import url('../../static/css/common.css');
  .infos{
    padding-left: .1rem;
  }
  .lists li{
    list-style-type:circle;
    margin-left: .4rem;
    padding: .2em;
  }
</style>
