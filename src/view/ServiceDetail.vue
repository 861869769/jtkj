<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">相关服务</div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
            <p>特色服务</p>
            <li
              :class="item.id==id?'active':''"
              v-for="(item,index) in serviceNavList"
              :key="index"
            >
              <a :href="'#'+item.id">{{item.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div class="content-block" v-for="(item,index) in serviceContentList" :key="index">
            <h2 :id="item.id">
              {{item.title}}
              <small>/ {{item.eng_title}}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "软件定制开发"
        },
        {
          id: "section-2",
          title: "IT外包服务"
        },
        {
          id: "section-3",
          title: "网上商城建设"
        },
        {
          id: "section-4",
          title: "iOS应用定制开发"
        }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "软件定制开发",
          eng_title: "Customize App",
          content:
            "<h3>1、针对性强，适应性好</h3><p>\n" +
            "定制的企业所实施的信息系统是由专门的软件开发公司为其量身定做，充分发挥了企业个性化的优势，按照企业不同的经营理念、管理方针、业务流程的需求，既要基于现状，又在推进管理变革的基础上超越现状。因而定制的软件可操作性强，应用针对性强。\n" +
            "<h3>2、易用性强，可操作性好</h3>\n" +
            "定制开发的软件是根据企业需求与面向使用者进行需求调研后再进行专项开发，加上定制软件完全是根据企业现有的工作流程来编制的程序，所以系统功能条理清晰，结构严谨，简单易懂，面向员工的操作界面，使用起来方便\n" +
            "<h3>3、利用率高，性价比极高</h3>\n" +
            "一般通用版软件包含了各行各业各种管理模式和繁多的功能，但是，对于企业来说不可能都加以应用，系统一旦经过大量的剪裁和设置，一些特定企业仅用了通用版软件中很少一部分功能。而软件定制开发可以根据你不使用某些模块减掉这块的费用，这样不仅提高了软件的运行速度，也为企业节省了费用。\n" +
            "\n</p>"
        },
        {
          id: "section-2",
          title: "IT外包服务",
          eng_title: "Outsourcing",
          content:
            "<h3>什么是it外包</h3><p>IT外包服务（IT Outsourcing Managed Service）就是把企业和个人的信息化建设工作交给专业化服务公司来做。研究表明，服务效率更高，成本更低，升级更容易。它可以包括以下内容：信息化规划（咨询）、设备和软件选型、网络系统和应用软件系统建设、整个系统网络的日常维护管理和升级等。IT外包服务是企业迅速发展企业数字化，提高数字化质量、提高企业工作效率，节约信息化成本的一种途径，也为个人用户提供巨大的帮助。</p>"
        },
        {
          id: "section-3",
          title: "网上商城建设",
          eng_title: "eCommerce Site",
          content:
            "<h3>公众号/小程序</h3><p>一、成本低\n" +
            "\n" +
            "　　与各大电商平台相比，小程序入驻的获客成本和交易成本较低。因为依靠微信的11亿活跃用户，小程序具有天生自然流量的属性，与此同时还有众多的入口可以做为流量变现，比如公众平台的内容变现，微信群的社交变现，现在朋友圈还可以直接跳转小程序。渠道的众多，除了充分利用自身资源以外，还可以找到性价比更高的第三方服务平台进行合作。\n" +
            "\n" +
            "二、用户体验好\n" +
            "\n" +
            "　　在微信端的入口随处可见， 利用社交、熟人圈进行分享、传播，不需要下载，点击即可体验商品，参加活动，支付下单，甚至还有留存、复购等营销手段。\n" +
            "\n" +
            "　三、购买效率高\n" +
            "\n" +
            "　　小程序大大的减少了购买的步骤，让支付变得更简单粗暴，无论在任何一个页面都可以直接下单进行支付，缩短了购买的时间，提高了购买的效率，不留给用户犹豫的时间。\n" +
            "\n" +
            "　　小程序和其他电商最大的一个区别是，去中心化，小程序让电商更加垂直，可以主动的触达到我们精准的用户群，第一时间给到用户最想要的，而不是被动的等待用户来搜索、关注、收藏，甚至是哪一天突然想起你。</p>"
        },
        {
          id: "section-4",
          title: "iOS应用定制开发",
          eng_title: "iOS App Dev",
          content:
            "<h3>iOS</h3><p>IOS是基于iPhone开发的操作系统，在移动终端用户众多，用户粘性较大。苹果IOS App Store里面的应用软件的数量、活跃度和下载次数在应用软件市场处于领先地位。\n" +
            "\n" +
            "IPhone和 iPad都是高端型的产品，其用户具有较高消费能力。接下来，酬诚众包平台小编为您具体介绍下IOS APP的开发优势。\n" +
            "\n" +
            "相同的一个应用，同时在安卓与苹果平台上发布运营，其用户愿意进行消费的，一部分原因可能由于 iPhone 用户的确比较富足，另一部分原因则在于 iTunes 与信用卡之间的整合，其支付方式十分便捷。\n" +
            "\n" +
            "苹果用户想要下载任何软件都只能在App Store应用商店中下载，相对于安卓有海量的应用商店，而苹果的唯一性，提升了软件的安全问题，同时也减少了应用方在多平台上维护的费用。</p>"
        }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}
ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}
ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}
ul.nav-tabs li:first-child {
  border-top: none;
}
ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}
ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}
ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}
ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}
ul.nav-tabs.affix {
  top: 30px;
}
.content-block {
  margin: 50px 0;
}
.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
