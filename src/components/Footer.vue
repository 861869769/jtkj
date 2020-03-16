<template xmlns="http://www.w3.org/1999/html">
  <div id="footer" class="container-fluid">
    <div class="logo">
      <img src="@/assets/img/logo_white.png" alt="logo图">
    </div>
    <p class="title">宁波蓝草科技有限公司</p>
    <p class="address_tel_fax">
      <span>地址：宁波市鄞州区海晏南路116弄恒大城市之光广场2幢714室</span>
    </p>
    <p class="email_wx">
      <span>Tel:18358408813 &#12288;</span>
      <span>邮箱:lancao0311@163.com &#12288;</span>
      <span>公司微信号:lancao0311</span>
    </p>
    <p class="copy">Copyright &copy; 2020 - 2021 宁波蓝草科技有限公司</p>
  </div>
</template>
<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>
<style scoped>
#footer {
  width: 100%;
  height: 100%;
  color: #fff;
  background: #474747;
  overflow: hidden;
  text-align: center;
}
.logo {
  width: 54px;
  height: 54px;
  margin: 50px auto 20px;
}
.title {
  font-size: 25px;
  margin-bottom: 20px;
}
.address_tel_fax {
  color: #d3d3d3;
  font-size: 14px;
  margin: 10px 0;
}
.email_wx {
  color: #d3d3d3;
  font-size: 14px;
}
.copy {
  color: #d3d3d3;
  font-size: 14px;
  margin: 50px 0 10px;
}
@media screen and (max-width: 997px) {
  .title {
    font-size: 20px;
  }
  .address_tel_fax {
    font-size: 12px;
  }
  .email_wx {

  font-size: 12px;
}
.copy {
  font-size: 12px;
  margin: 30px 0 10px;
}
}
</style>

