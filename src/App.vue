<script setup>
import { ref } from 'vue';
import HeaderPc from './components/HeaderPc.vue'
import HeaderSp from './components/HeaderSp.vue'
import FvCont from './components/FvCont.vue'
import TopNews from './components/TopNews.vue'
import TopConcept from './components/TopConcept.vue'
import TopAbout from './components/TopAbout.vue'
import TopFeature from './components/TopFeature.vue'
import TopAccess from './components/TopAccess.vue'
import FooterCont from './components/FooterCont.vue'


const siteTtl = ref("静茶店");

const siteNav = [
  {
    name: '静茶店のこと',
    link: '/'
  },
  {
    name: '商品紹介',
    link: '/'
  },
  {
    name:'ブログ',
    link: '/'
  },
  {
    name: '店舗情報',
    link: '/'
  },
  {
    name: 'お問い合わせ',
    link: '/'
  }
];
</script>

<template>
  <div>
    <header>
      <HeaderSp :siteTtl="siteTtl" :siteNav="siteNav" />
      <HeaderPc :siteTtl="siteTtl" :siteNav="siteNav" />
    </header>
    <FvCont />
    <div class="inner">
      <TopNews :siteTtl="siteTtl" />
    </div>
    <TopConcept :siteTtl="siteTtl" />
    <div class="inner">
      <TopAbout :siteTtl="siteTtl" />
    </div>
    <TopFeature :siteTtl="siteTtl" />
    <TopAccess :siteTtl="siteTtl" />
    <footer>
      <FooterCont :siteTtl="siteTtl" :siteNav="siteNav" class="l-footer" />
    </footer>
  </div>
</template>

<style scoped>
</style>
