<template lang="pug">
.container
  section.highlights.row.text-center
    .col-md(v-for="item in items", :key="item.img")
      img.rounded-circle.highlights-img(:src="item.img", alt="item.alt")
      h2 {{ item.title }}
      p {{ item.desc }}
      p #[a.btn.btn-secondary(:href="$withBase(item.btnUrl)", role="button") {{ item.btnText }}]
</template>

<script>
export default {
  props: ['items']
}
</script>

<style lang="sass" scoped>
  .highlights
    margin: 3rem 0
  .highlights-img
    width: 128px
</style>


