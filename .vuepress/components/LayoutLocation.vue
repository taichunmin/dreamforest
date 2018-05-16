<template lang="pug">
div
  section#location
    .jumbotron.bg-white.mb-0
      .container
        .row.pt-1
          .col-md-5
            h1 交通資訊
            hr.mb-5
            p 地址：40757 台中市西屯區市政路 402 號 7 樓<br>　　　（需在一樓換取感應卡後右側電梯上樓）
            p 電話：(04) 23692699
            p 粉專：#[a(href="https://www.facebook.com/dreamforest.org/", target="_blank") Dreamforest 夢森林]
          .col-md-7
            img.img-fluid.w-100(:src="$withBase('/images/location.svg')")
  section#google-maps
    <iframe width="100%" height="450" frameborder="0" style="border:0" src="https://www.google.com/maps/embed/v1/search?q=%E5%8F%B0%E7%81%A3%E5%8F%B0%E4%B8%AD%E5%B8%82%E8%A5%BF%E5%B1%AF%E5%8D%80%20%E5%BE%AE%E7%A8%8B%E5%BC%8F%E8%B3%87%E8%A8%8A%E8%82%A1%E4%BB%BD%E6%9C%89%E9%99%90%E5%85%AC%E5%8F%B8&key=AIzaSyCXboeblulLZEQ0BxjVXbl0Y8bVPW-jbNo" allowfullscreen></iframe>
  section#transit
    .container.my-4.text-center
      h1.text-center 自行前往
      .row.justify-content-md-center
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/drive-motorway.svg')")
          h5 高速公路（國道 1 號）
          p 南下、北上：中港交流道下往台中市市區，惠中路右轉、市政路右轉即可到達。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/5bBC3KoQ3Vk", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/drive-automobile.svg')")
          h5 中彰快速道路（台 74 號）
          p 由市政路閘道下，往市政路方向，惠中路左回轉慢車道。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/CPpDNL3cytB2", target="_blank") 於 Google Maps 開啟
  hr
  section#transit
    .container.my-4.text-center
      h1.text-center 大眾運輸
      .row
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-train.svg')")
          h5 臺鐵
          p 台中車站搭乘 75 號公車至第六分局站（市政路與惠來路口），步行 100 公尺即可抵達。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/66X5BMjtPw12", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-high-speed-train.svg')")
          h5 高鐵
          p 高鐵台中站搭乘 155 號公車至第六分局站（市政路與惠來路口），步行 100 公尺即可抵達。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/2fmtbTvikvB2", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-bus.svg')")
          h5 國道客運
          p 朝馬轉運站搭乘 75 公車至第六分局站（市政路與惠來路口），步行 100 公尺即可抵達。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/Vvct7UrGDh92", target="_blank") 於 Google Maps 開啟
  hr
  section#transit
    .container.my-4.text-center
      h1.text-center 停車場
      .row.justify-content-md-center
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/park-automobile.svg')")
          h5 汽車
          p
            div 市政路與惠來路延線之公有停車格 #[span.badge.badge-success 20/hr]
            div 市政北一路與惠來路公有立體停車場 #[span.badge.badge-success 30/hr]
            div 豐邑市政核心 B2 停車場 #[span.badge.badge-success 30/hr]
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/park-scooter.svg')")
          h5 機車
          p 市政路與惠來路延線之機車停車格 #[span.badge.badge-success Free]
</template>

<script>
export default {
  
}
</script>

<style lang="sass">
.img-transmit
  max-height: 128px
</style>
