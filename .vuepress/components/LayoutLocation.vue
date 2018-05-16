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
          img.my-3.img-transmit(:src="$withBase('/images/drive-hw1.svg')")
          h5 高速公路（國道 1 號）
          p.px-5 #[span.text-nowrap 中港交流道] ➜ #[span.text-nowrap 台 12 線往市區方向] ➜ #[span.text-nowrap 惠來路右轉] ➜ #[span.text-nowrap 抵達夢森林]。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/4opZH7NCLqL2", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/drive-phw74.svg')")
          h5 中彰快速道路（台 74 號）
          p.px-5 #[span.text-nowrap 市政路閘道] ➜ #[span.text-nowrap 市政路] ➜ #[span.text-nowrap 抵達夢森林]。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/CPpDNL3cytB2", target="_blank") 於 Google Maps 開啟
  hr
  section#transit
    .container.my-4.text-center
      h1.text-center 大眾運輸
      .row
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-train.svg')")
          h5 臺鐵
          p #[span.text-nowrap 台中車站] ➜ #[span.text-nowrap 公車 #[code 75] 往臺中榮總] ➜ #[span.text-nowrap 第六分局（惠來路）下車] ➜ #[span.text-nowrap 抵達夢森林]。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/66X5BMjtPw12", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-high-speed-train.svg')")
          h5 高鐵
          p #[span.text-nowrap 高鐵台中站] ➜ #[span.text-nowrap 公車 #[code 155] 往麗寶樂園] ➜ #[span.text-nowrap 第六分局（市政路）下車] ➜ #[span.text-nowrap 抵達夢森林]。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/2fmtbTvikvB2", target="_blank") 於 Google Maps 開啟
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/transmit-bus.svg')")
          h5 國道客運
          p #[span.text-nowrap 朝馬轉運站] ➜ #[span.text-nowrap 公車 #[code 75] 往一江橋] ➜ #[span.text-nowrap 第六分局（惠來路）下車] ➜ #[span.text-nowrap 抵達夢森林]。
          a.btn.btn-primary.text-white(href="https://goo.gl/maps/6aN2gp8NJ8K2", target="_blank") 於 Google Maps 開啟
  hr
  section#transit
    .container.my-4.text-center
      h1.text-center 停車場
      .row.justify-content-md-center
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/park-automobile.svg')")
          h5 汽車
          p
            div 市政路、惠來路與惠中路之路邊停車格 #[code $20/h]
            div 臺中市惠來立體停車場 #[code $30/h]
            div 豐邑市政核心 B2 停車場 #[code $30/h]
        .col-md
          img.my-3.img-transmit(:src="$withBase('/images/park-scooter.svg')")
          h5 機車
          p 市政路、惠來路與惠中路之路邊停車格 #[code Free]
</template>

<script>
export default {
  
}
</script>

<style lang="sass">
.img-transmit
  max-height: 128px
</style>
