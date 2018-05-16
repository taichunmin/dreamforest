<template lang="pug">
  section.carousel.slide(:id="id", data-ride="carousel")
    ol.carousel-indicators(v-if="indicators")
      li(v-for="item, index in items", :key="item.img", :data-target="'#' + id", :data-slide-to="index", :class="{active: index === 0}")
    .carousel-inner
      .carousel-item(v-for="item, index in items", :key="item.img", :class="{active: index === 0}")
        .carousel-img(:style="{'background-image': `url(${item.img})`, 'background-position': item.imgpos || 'center center'}")
          img.d-block.w-100(:src="item.img", :alt="item.alt || ''")
        .carousel-caption.d-none.d-md-block
          slot(:item="item", :index="index")
    a.carousel-control-prev(:href="'#' + id", role="button", data-slide="prev", v-if="controlPrevNext")
      span.carousel-control-prev-icon(aria-hidden="true")
      span.sr-only Previous
    a.carousel-control-next(:href="'#' + id", role="button", data-slide="next", v-if="controlPrevNext")
      span.carousel-control-next-icon(aria-hidden="true")
      span.sr-only Next
</template>

<script>
export default {
  props: {
    items: Array,
    indicators: {
      type: Boolean,
      default: true
    },
    controlPrevNext: {
      type: Boolean,
      default: true
    },
  },
  computed: {
    id () {
      return 'carousel-' + this._uid
    }
  }
}
</script>

<style lang="sass" scoped>
.carousel-img
  max-height: 30rem
  background-size: cover
  background-repeat: no-repeat
  img
    visibility: hidden
</style>
