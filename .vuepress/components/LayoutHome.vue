<template lang="pug">
  .layout-home
    BootstrapCarousel(:items="$page.frontmatter.carousel")
      template(slot-scope="{ item }")
        .container(v-if="item.title")
          .carousel-caption(:class="'text-' + (item.align || 'left')")
            h1 {{ item.title }}
            p(v-if="item.desc") {{ item.desc }}
            p(v-if="item.btnText")
              a.btn.btn-lg.btn-primary(:href="$withBase(item.btnUrl)", role="button") {{ item.btnText }}
    .container
      section.row.text-center.my-4
        .col-md(v-for="item in $page.frontmatter.highlights", :key="item.img")
          img.my-3.rounded-circle.highlights-img(:src="item.img", alt="item.alt")
          h5 {{ item.title }}
          p {{ item.desc }}
          p #[a.btn.btn-secondary(:href="$withBase(item.btnUrl)", role="button") {{ item.btnText }}]
</template>

<style lang="sass" scoped>
  .highlights-img
    max-height: 128px
</style>
