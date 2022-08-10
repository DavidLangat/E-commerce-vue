<template>
    <HomeMe />
    <MyCate />
    <OnSale />
    <MyOffer />
</template>
<script>
import OnSale from '@/components/onsale.vue'
import HomeMe from '@/components/home.vue'
import MyCate from '@/components/category.vue'
import MyOffer from '@/components/offer.vue'
export default {
  name: 'HomeView',
  components: {
    HomeMe, OnSale, MyCate, MyOffer
  }
}
</script>
