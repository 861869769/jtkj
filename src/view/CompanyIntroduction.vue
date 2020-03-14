<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>宁波蓝草科技有限公司</h3>
                    <p class=".text-justify">宁波蓝草科技有限公司（以下简称蓝草科技）位于浙江省宁波市鄞州区，是一家集平台技术设计及专业服务的软硬件智能应用技术服务企业。</p>
                    <p class=".text-justify">蓝草科技倡导诚信、专业、高效的企业精神，以结果为导向，以创新为核心，以服务为支持，致力于为政府、企业、个人提供专业的APP定制、小程序定制、WEB设计等一站式产品设计与维护。</p>
                  <p class=".text-justify">蓝草科技的以专业团队将立足于您的业务及信息化目标，开发和维护符合您的业务特色的具有价值应用性的软件。</p>
                  <p class=".text-justify">蓝草科技本着“高效·创新·自信”的企业信念，将抓住机会与挑战，坚持以特色为重要手段，加大创新力度，提升产品的运作能力，立志于打造“具有特色的中国优秀互联网企业”。</p>

                </div>
            </div>
        </div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{

        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 100px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

