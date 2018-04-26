---
layout: LayoutHome
carousel:
  - img: https://i.imgur.com/CWPzlSU.jpg
    title: Example headline.
    desc: Cras justo odio, dapibus ac facilisis in, egestas eget quam. Donec id elit non mi porta gravida at eget metus. Nullam id dolor id nibh ultricies vehicula ut id elit.
    btnText: Sign up today
    btnUrl: '#'
  - img: https://i.imgur.com/8Usqyv7.jpg
    title: Another example headline.
    desc: Cras justo odio, dapibus ac facilisis in, egestas eget quam. Donec id elit non mi porta gravida at eget metus. Nullam id dolor id nibh ultricies vehicula ut id elit.
    btnText: Learn more
    btnUrl: '#'
    align: center
  - img: https://i.imgur.com/qAreRvb.jpg
    title: One more for good measure.
    desc: Cras justo odio, dapibus ac facilisis in, egestas eget quam. Donec id elit non mi porta gravida at eget metus. Nullam id dolor id nibh ultricies vehicula ut id elit.
    btnText: Browse gallery
    btnUrl: '#'
    align: right
highlights:
  - img: https://i.imgur.com/sxUto1j.png
    alt: 社群交流
    title: 社群交流
    desc: Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod. Nullam id dolor id nibh ultricies vehicula ut id elit. Morbi leo risus, porta ac consectetur ac, vestibulum at eros. Praesent commodo cursus magna.
    btnText: View details »
    btnUrl: /
  - img: https://i.imgur.com/YnnYbfj.png
    alt: 專業論壇
    title: 專業論壇
    desc: Duis mollis, est non commodo luctus, nisi erat porttitor ligula, eget lacinia odio sem nec elit. Cras mattis consectetur purus sit amet fermentum. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh.
    btnText: View details »
    btnUrl: /
  - img: https://i.imgur.com/RiOuIv4.png
    alt: 產業發展
    title: 產業發展
    desc: Donec sed odio dui. Cras justo odio, dapibus ac facilisis in, egestas eget quam. Vestibulum id ligula porta felis euismod semper. Fusce dapibus, tellus ac cursus commodo, tortor mauris condimentum nibh, ut fermentum massa justo sit amet risus.
    btnText: View details »
    btnUrl: /
---

<BootstrapCarousel :items="$page.frontmatter.carousel">
  <template slot-scope="{ item }">
    <div class="container" v-if="item.title">
      <div class="carousel-caption" :class="'text-' + (item.align || 'left')">
        <h1>{{ item.title }}</h1>
        <p v-if="item.desc">{{ item.desc }}</p>
        <p v-if="item.btnText"><a class="btn btn-lg btn-primary" :href="$withBase(item.btnUrl)" role="button">{{ item.btnText }}</a></p>
      </div>
    </div>
  </template>
</BootstrapCarousel>
<Highlights :items="$page.frontmatter.highlights"></Highlights>